---
tags: NumPy
---


# 2021-04-28 NumPy Community Meeting

Note: we now alternate between [triage meetings](https://hackmd.io/68i_JvOYQfy9ERiHgXMPvg) and community meetings.

- Time: 20:00 UTC
- Join via Zoom at https://berkeley.zoom.us/j/762261535 (or [dial-in](https://berkeley.zoom.us/u/aC3ENhycM))
- [Trello workboard](https://trello.com/b/Azg4fYZH/numpy-at-bids)
- [Previous community meetings](https://github.com/numpy/archive/tree/master/status_meetings)
- [Previous triage meetings](https://github.com/numpy/archive/tree/master/triage_meetings)
- [Documentation team meetings](https://hackmd.io/oB_boakvRqKR-_2jRV-Qjg)


**Present:** Ralf, Chuck , Sebastian, Melissa, Mars, Inessa, Kiran Khanna, Ryan, Tony Fast


## Follow-up from last meeting / discussions

- NumPy Open Collective claimed.

- Reminder: NumPy WiMLDS sprint on May 9th. Help with preparing issues beforehand & PR review on the day will be very welcome.

- Accessibility Discussion - Review of NumPy Documentation and Website


## Topics

- NumFOCUS subcommittee met last week to review the NumPy finances (Thomas Caswell, Melissa, Sebastian, Ralf).
    - A few issues found, NumFOCUS is working on addressing those.

- SciPy 2021 Sprint? (July 17-18)


- 2020 Community Survey results .pdf report is 99% ready.


- (Sebastian) I don't want to spend too much time on this, but if we agree on giving "weak python scalar promotion" a shot... how would we go about?  Right now I am operating under the assumption that this will  happen.  I assume any attempts are too late for the next release, but should we plan to just rip off the band-aid after branching and see where it takes us?
    - We will try this after the release (hopefully no revert will be necessary)

- Accessibility Discussion
  - Almost all issues in the theme, although e.g. alt-texts need fixing.
  - pydata-sphinx theme requires testing: https://github.com/pydata/pydata-sphinx-theme/pull/294

- List of NumPy functions and frequency of use, as measured in other libraries (SciPy, Pandas, etc.): https://github.com/Quansight-Labs/python-api-inspect/blob/master/data/csv/numpy-summary-without-tests.csv



---

Please remember to archive this file and commit it to github.com/numpy/archive
