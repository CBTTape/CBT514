# CBT514
Converted to GitHub via [cbt2git](https://github.com/wizardofzos/cbt2git)

This is still a work in progress. 
Due to amazing work by Alison Zhang and Jake Choi repos are no longer deleted.

```
//***FILE 514 is from Larry Williams and contains an ICHRTX00 SAF   *   FILE 514
//*           router to allow a volume or volumes to be treated     *   FILE 514
//*           as special read only volume(s).  Not even RACF        *   FILE 514
//*           "Special" users can update files there.               *   FILE 514
//*                                                                 *   FILE 514
//*           This was designed to solve a problem with code that   *   FILE 514
//*           had been shipped to our customers (which should       *   FILE 514
//*           have then  been "frozen" forever) being updated at    *   FILE 514
//*           our site (a software vendor) by mistake, disrupting   *   FILE 514
//*           the "audit trail" of what had actually been shipped   *   FILE 514
//*           to our customers.                                     *   FILE 514
//*                                                                 *   FILE 514
//*           This made it very difficult to debug programs at      *   FILE 514
//*           the customer site, since the code no longer           *   FILE 514
//*           matched.                                              *   FILE 514
//*                                                                 *   FILE 514
//*           The code contains a table of the allowed users who    *   FILE 514
//*           can do the updates.  All other users will ABEND       *   FILE 514
//*           913-0C (or DASDM alloc fail) trying to update.        *   FILE 514
//*                                                                 *   FILE 514
//*           You'll probably find this code interesting to look    *   FILE 514
//*           at, if you need protect some volume(s) from           *   FILE 514
//*           alteration by (almost) all users regardless of RACF   *   FILE 514
//*           authority.  I haven't tested the idea yet, but        *   FILE 514
//*           perhaps this might be an interesting way to lock up   *   FILE 514
//*           a "SYS1.PARMLIB" perhaps...                           *   FILE 514
//*                                                                 *   FILE 514
//*           The usual disclaimer applies: You use this at your    *   FILE 514
//*           own risk.  It has worked well at my site, your        *   FILE 514
//*           mileage may vary.                                     *   FILE 514
//*                                                                 *   FILE 514
//*           email:   larryw@ix.netcom.com                         *   FILE 514
//*                                                                 *   FILE 514
```
