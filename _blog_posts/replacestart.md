---
layout: none
---
<p class="pemp"><a class="prev" href="/articles/whynottrump/"><span class="hide">Previous post: Why Not Trump</span>
        < </a>
          Replace Start Menu on Windows
  <p class="pbody">
            I use two main tools to replace the start menu. The first is <a class="inline"
              href="https://learn.microsoft.com/en-us/windows/powertoys/run">Powertoys Run</a> (or <a class="inline"
              href="https://www.flowlauncher.com/">Flow Launcher</a>) and the second is <a class="inline"
              href="https://www.voidtools.com/downloads/">Everything for Windows</a>. There is also an <a class="inline"
              href="https://github.com/lin-ycv/EverythingPowerToys">Everything plugin</a> for both Powertoys Run and
            Flow Launcher. This allows me to use a hotkey to search for any file on my system, and because of the way
            Everything indexing works, it's very fast.
          </p>
  <p class="pbody">
            I also use this Autohotkey Script to disable the Windows key, but retain its combinations (such as WIN+Arrow
            Keys):
      <blockquote>
            ;Disable LWin press and retain its combos
            <br>~LWin::vk07
          </blockquote>
    </p>
<p class="pbody">
      And this script to hide the taskbar, in combination with the vanilla auto-hide functionality. This hides the
      taskbar or shows it again when CTRL + ALT + = is pressed.
<blockquote>
      ^!=:: ;Ctrl + Alt + = : Hide taskbar
      <br>If WinExist("ahk_class Shell_TrayWnd")
      <br>{
      <br> WinHide, ahk_class Shell_TrayWnd
      <br> WinHide, ahk_class Shell_SecondaryTrayWnd
      <br>}
      <br>Else
      <br>{
      <br> WinShow, ahk_class Shell_TrayWnd
      <br> WinShow, ahk_class Shell_SecondaryTrayWnd
      <br>}
    </blockquote>
    </p>
<p class="pbody">
      You can find the rest of my Autohotkey Scripts <a class="inline"
        href="https://github.com/wfurney13/dotfiles/blob/master/ahk/hotkeys.ahk">on my Github.</a> I've tried to leave
      comments so that it's obvious what everything does. If you want a more stylish taskbar replacement, I recommend <a
        class="inline" href="https://github.com/glzr-io/zebar">Zebar</a> in combination with <a class="inline"
        href="https://github.com/glzr-io/glazewm">GlazeWM</a>. I may make a seperate post about Zebar and GlazeWM when I
      have a better configuration and Zebar has been updated some more.
    </p>