---
layout: none
---
<p class="pemp"><a class="prev" href="/articles/useyt/"><span class="hide">Previous post: Make YouTube Usable
          (Again)</span>
        < </a>What's all wrong with this SQL?<a class="next" href="/articles/24tte/"> > <span class="hide">Next Post: 2024
              Trip to Europe</span> </a></p>
<p class = "pbody">
      How many more issues can you spot with this SQL? Here's how I would re-write it.
</p>

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

<p class = "pbody">
      And yes, <a class="inline" href='https://postimg.cc/Jth9sycN' target='_blank'>ChatGPT can spot the FLOAT
        issue.</a>
    </p>
