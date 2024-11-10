---
layout: article
---
* auto-gen TOC:
{:toc}
<a class="prev" href="/articles/useyt"> < </a><a class="next" href="/articles/24tte"> > </a>

## What's all wrong with this SQL?

Take a look at this *gorgeous* SQL I found on the internet. *Forget DATETIME, store "Day" as a varchar and (wait, what?) How many more issues can you spot?*  

<img src="/img/wwwsql.png">
                        
Here's how I would re-write it:

```sql
CREATE TABLE dbo.STORE_SALES (
ss_id INT IDENTITY(1,1) NOT NULL PRIMARY KEY,
ss_dateinserted DATETIME NOT NULL,
ss_wkr_id INT NOT NULL,
ss_amount DECIMAL(10,2) NOT NULL,
CONSTRAINT FK_STORESALES_WORKER FOREIGN KEY (ss_wkr_id)
REFERENCES dbo.WORKERS (wkr_id)
);
```

## And yes, [ChatGPT](/img/Chat-GPT-sees-the-issue.png) can spot the FLOAT issue.

