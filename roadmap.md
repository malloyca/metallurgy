# Development Roadmap

## TODO List

## Project Writeup
- Implementation
  - Analysis
    - Onset algorithm
      - Complex analysis version
    - pitch detection algorithm
      - PitchMelodia I think.
    - Data collected in a numpy array and passed to the synthesis component of the system.
  - Synthesis
    - Wavio in order to load 24-bit wav files (scipy not able to).
    - Straightforward, but bespoke functions to add samples, do basic processing, etc.
    - Can add more.
- Problem addressed (Failures we learned from)
  - Onset detection algorithm
    - Tested different versions, HFC gave false positives (add figure)
  - We were using the wrong pitch detection algorithm. Originally used `PredominantPitchMelodia`, gave wrong results.
    - `PitchMelodia` gave better results.
    - Also tried `PitchYin` and `PitchYinFFT`, but got worse results.
    - These were informal comparisons.
    - This is why a more quantitative, methodical study comparing different pitch detection algorithms on the steelpan would be helpful.
  - Next pitch value gave terrible results -> set it up for onset-to-onset avg/median
- Testing -> Rename as 'Results'
  - Make more test files.
    - Compare test file output against "ground truth".
    - Use float midi values against original integer midi values.
    - Add this data to testing section of paper.
    - Compare next pitch value against 5ms avg/median against onset-to-onset avg/median.
  - Other stuff?
- Current state
  - Delete this section
- Future plans
  - ML-based pitch detection algorithm
    - Goal is for a live, realtime usable pitch detector with minimal (<5ms latency).
  - Do a more comprehensive study comparing the accuracy of different pitch detection algorithms on the steelpan.

  
## From meeting with George
- Make more Audio test examples
  - Make MIDI versions
  - Make function to convert MIDI file to numpy array version for comparison
- Pitch detection algorithm comparison (makes each notebook file)
- Write report (Write about each project, background: onset detection, pitch detection and Steelpan acoustics)
- Longer term project: evaluate pitch detection algorithms on the steelpan

## Future plans:
- Machine learning based pitch detection system.
  - The pitch detection algorithms included in Essentia are failing on the test input (which is Twinkle Twinkle Little Star).
  - There is clearly room for improvement in this area.
  - We should devise an ML and/or deep learning based steelpan pitch detection system to test against the Essentia (and/or Librosa?) algorithms.
- Do other awesome work.
