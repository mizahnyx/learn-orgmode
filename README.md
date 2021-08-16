# About this file

  - I add new things I learn about Emacs and orgmode here.
  - I formulate questions about where I stumbled, marked :WIP:

# Starting Emacs

## Minimal pipeline

  - Install emacs on WSL with `sudo apt-get install emacs`
  - Launch emacs with `emacs` command
  - Open a file with F10 menu
  - Edit file using orgmode
  - Save file **C-x C-s**
  - Exit Emacs **C-x C-c**

<div class="INSTALL drawer">

  - Running in cmder bash (ubuntu)
  - Windows Emacs MSI (bad russian font spacing)
  - VSCode extension (no agenda view)

</div>

## Improvements

  - F10 may need Fnlock to work on Lenovo - use Fn-Esc.
  - Configure terminal to resolve [key binding
    conflicts](https://emacs.stackexchange.com/questions/68105/how-to-use-ctrl-c-on-wsl-key-binding-conflict)
    like Ctrl-C. See also `org-disputed-keys` in [Orgmode
    conflicts](https://orgmode.org/manual/Conflicts.html).
  - Launch emacs with filename `emacs -nw README.org`
  - Use Shift for selection and CUA mode with more familiar key
    bindings.
  - `pandoc README.org -f org -t gfm -o README.md` (see pandoc [formats
    list](https://pandoc.org/MANUAL.html#general-options))

## Emacs configuration

### Where is the config?

  - \~/.emacs is a file
  - \~/.emacs.d is a directory
  - QUESTION: what is the difference?

### Set `org-support-shift-select` and CUA option

  - Selecting with Shift is already built-in part of Emacs, but not
    org-mode
  - Start with 'M-x customize' to find options about Shift selection
  - Set CUA (Ctrl-Z/X/C/V) as part of F10 menu

# Questions <span class="tag" data-tag-name="WIP"><span class="smallcaps">WIP</span></span>

### Attempting X410 video system

  - <https://emacsredux.com/blog/2020/09/23/using-emacs-on-windows-with-wsl2/>
  - QUESTION: starts with two windows, must disable the tutorial window
  - works now\!
  - TODO: must buy from Windows store while discoutn lasts

### Wanted \[0/2\]

Specific:

  - \[ \] Move line across headers, beyond own section (Alt - arrow has
    limits within a header)
  - \[ \] What does bottom line with `-UUU(DOS)**--F1` mean? What is it
    called? How to remove it?
  - \[ \] Make internal link in document

General:

  - \[ \] How does find and replace work?
  - \[ \] Good workflow samples and file samples to learn from

### Not critical \[0/5\]

  - \[ \] Recalulcate list stats (I double click C-c C-c now to toggle
    and recalculate)
  - \[ \] Add timestamp with current time, not just date
  - \[ \] Change selection color to lightblue (I did, but it did not
    save)
  - \[ \] View calendar
  - \[ \] TOC

### Not todo

Things that are not a priority, on a cost-benefit basis:

  - Editing configuration extensively
  - Using elisp
  - Use spacemacs or emacs-doom

Other reasons:

  - Fix wrong spacing of Russian fonts in Windows MSI Emacs GUI
  - [Reload on file
    change](https://emacs.stackexchange.com/questions/169/how-do-i-reload-a-file-in-a-buffer?newreg=a3feb7dd0515464f962f420449b8f1a5)
    (will allow editing in VS Code)

# Using orgmode

## \<TAB\> is all you need

  - TAB shows/hides headers (quite powerful\!)
  - Shift-TAB opens all headers

## Getting around headers

  - Alt + left rightor changes header level
  - Alt + up or down moves lines around
  - Shift - arrow:
      - changes list numbering style
      - cycles TODO-DONE in header
      - selects in CUA mode

## Create a hyperlink

Use `[[url][]]` syntax or C-c C-l TODO: hyperlinks inside documents.

## Use timestamps

SCHEDULED: \<2021-08-15 Sun\>

As
[guide](https://orgmode.org/guide/Creating-Timestamps.html#Creating-Timestamps)
suggests:

  - C-c . for timestamp
  - S-arrow for change
  - QUESTION: How to put a timestamp with time, not just date?

## Checkboxes

  - You must type \[0/0\] or \[0%\] for checkbox
  - Only X counts for completion, not \`x\` or \`+\`
  - C-c C-c toggles and recalculates
  - QUESTION: what can recalcultae on its own?
  - Check Rainer König video [OrgMode E01S05:
    Checklists](https://www.youtube.com/watch?v=gvgfmED8RD4&list=PLVtKhBrRV_ZkPnBtt_TD1Cs9PJlU0IIdE&index=5&t=444s)

Sample checkbox list \[2/3\], \[66%\]:

  - \[X\] Item 1
  - \[X\] Item 2
  - \[ \] Item 3

## Agenda

  - Use F10 and menu
  - C-a key binding must be configured

Question
<span class="tag" data-tag-name="QUESTION"><span class="smallcaps">QUESTION</span></span>

  - How to close agenda buffer

## Make a selection, copy and paste selection

## Other tasks

  - Sort this list based on completion is C-c ^

  - Add more cycling todo tags `#+SEQ_TODO:`

  - Archive tasks with menu

  - Defintion list with `::` separator

  - 
# Reference

## Concepts

  - buffer  
    a screen that represents a file or Emacs own output
  - frame  
    …
  - window  
    …

## Notation

\- \* is always a header

  - drawer box has :NAME: and :END:

## Quotes

\-[ @Trevoke via
reddit](https://www.reddit.com/r/emacs/comments/42qr9h/orgmode_for_gtd/d0fupy5?utm_source=share&utm_medium=web2x&context=3):

> The best advice I've heard for using org-mode in some sort of GTD
> system was not to try and set up categories when you start. Start with
> just a bunch of TODOs, and slowly grow the system as you feel the need
> to.

# Links

## Videos

Essential:

  - [Carsten Dominik keynote
    (2008)](https://www.youtube.com/watch?v=oJTwQvgfgMM)
  - [Rainer König lesson
    series](https://www.youtube.com/playlist?list=PLVtKhBrRV_ZkPnBtt_TD1Cs9PJlU0IIdE)

Extension:

  - [Evil Mode: Or, How I Learned to Stop Worrying and Love
    Emacs](https://www.youtube.com/watch?v=JWD1Fpdd4Pc)
  - [Andrew Tropin - Modern Emacs
    (2021)](https://www.youtube.com/watch?v=ZbxUJz6a9Io)

Academic:

  - [On the design of text editors](https://arxiv.org/abs/2008.06030)

## Blogs and success stories

  - <https://sachachua.com/blog/2014/01/tips-learning-org-mode-emacs/>
  - <https://blog.aaronbieber.com/2016/09/24/an-agenda-for-life-with-org-mode.html>

## Orgfiles on github

  - <https://github.com/abcdw/notes/blob/master/notes/20210805075718-the_modern_emacs.org>
