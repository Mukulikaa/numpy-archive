# 2019-12-11 NumPy Community Meeting

**Next community call is 8 January 2020**

Note: we now alternate between community meetings and [triage meetings](https://hackmd.io/68i_JvOYQfy9ERiHgXMPvg).

- Time: 11am Pacific Time
- Join via Zoom at https://berkeley.zoom.us/j/762261535 (or [dial-in](https://berkeley.zoom.us/u/aC3ENhycM))
- [Trello workboard](https://trello.com/b/Azg4fYZH/numpy-at-bids)
- [Previous community meetings](https://github.com/numpy/archive/tree/master/status_meetings)
- [Previous triage meetings](https://github.com/numpy/archive/tree/master/triage_meetings)

**Present:** Inessa Pawson, Warren Weckesser, Matti Picus, Sebastian Berg, Chuck Harris, Hameer Abbasi, Ralf Gommers, Stéfan van der Walt, Ross Barnowski

**This meeting will focus on Community topics. Next week's will focus on Issue and Pull Request Triage**

## Follow-up from last meeting / discussions

- [Milestones](https://github.com/numpy/numpy/milestone/69) for 1.18 release
    - [reverting speedups](https://github.com/numpy/numpy/issues/13958) is now done for 1.18. Will try the clean fix in 1.19/master after branching

- [Milestones](https://github.com/numpy/numpy/milestone/78) for 1.17.5 release

- Progress on numpy.org web site:
  - [December'19 Web Team Meeting notes](https://github.com/numpy/archive/blob/master/status_meetings/webteam_meeting2019-12-10.md)

  - Translations will focus on Mandarin (important, and we have a volunteer)
  - Surge deployment doesn't work from PRs, this is a GitHub Actions limitation, Shekhar is looking at changing to TravisCI or CircleCI.
  - Local build is really easy:
      - Clone `https://github.com/numpy/numpy.org`
      - `git submodule update --init`
      - `make` -> hosts at `http://localhost:1313`
      - N.b. make sure you have hugo installed

- [API prioritization](https://gist.github.com/seberg/0fcd995a34ee31a9b7fe7bbc924b7c8f) <-- Run this notebook, fill out the generated questionnaire, and send Sebastian the generated text file!
  - Also see [Python API inspect](https://github.com/Quansight-Labs/python-api-inspect)

## Topics

**Next community call is 8 January 2020**

- Docs calls and documentation team will continue after the end of GSOD
 
- [cygwin compilation](https://github.com/numpy/numpy/issues?utf8=%E2%9C%93&q=is%3Aopen+cygwin+) There are a few open issues with this platform. Is it a priority?
  - Let's make a list of all the platforms we support and what does/doesn't work

- The triage meeting notes are now on a [different doc](https://hackmd.io/68i_JvOYQfy9ERiHgXMPvg)

 - Ragged arrays: modified NEP. Is `np.allow_ragged` the best we can do?
    - https://github.com/matplotlib/matplotlib/pull/15833
    - https://github.com/pandas-dev/pandas/pull/30035

- SIMD progress
  - [draft NEP](https://github.com/mattip/numpy/pull/42) needs filling out
  - [runtime cpu feature detection PR 13421](https://github.com/numpy/numpy/13421) and [enable multi-platform SIMD compiler optimizations PR 13516](https://github.com/numpy/numpy/pull/13516)
  - Test the two PRs together, do they work?
  - Ask specific questions to complete the NEP

- poly1d / Polynomial fixes suggested plan; for Chuck's attention
  1. poly1d does not pretend to be an array any longer
  2. Fix poly1d array priority
  3. Polynomial class should have _repr_ to do fancy printing in IPython / Jupyter
  4. Polynomial class should support symbol; catch when trying to multiple polys of different symbols
  5. Update poly1d docstring to warn against using it, referring users to Polynomial


- Should the clarification about linalg be extended to revisiting `np.dual`? This api sounds great but it isn't clear which function is used when and how the choice is made. I found it  particularly confusing given the recent improvements to fft in SciPy, as well as due to some of the difference in the fft implementations accross SciPy and NumPy. KS (bashtage)
  - Good candidate for deprecation

- Twitter account: super short bikeshedding session, decided on `numpy-team`.

## Additional Details

- Matti

- Warren
  - [PR](https://github.com/numpy/numpy/pull/14988) for [Trello card on "Inform users on usage of `scipy.linalg`, `np.linalg`"](https://trello.com/c/0rXuCoql/70-inform-users-on-usage-of-scipylinalg-nplinalg) is awaiting next round of review.
      
  - My repo [ufunclab-wheels](https://github.com/WarrenWeckesser/ufunclab-wheels) is a test of using multibuild in a GitHub Actions workflow to build wheels.

- Sebastian
  - Reactivated Reference counting
  - Created an optimized argument parser as a drop in for almost all argparsing.


---

Please remember to archive this file and commit it to github.com/numpy/archive

