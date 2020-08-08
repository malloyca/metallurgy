# Development Roadmap

## TODO List
- Move `Steel-Drum-project.ipynb` from the root directory to `/Source/`.
  - Check `Steel-Drum-project.ipynb` to make sure this doesn't break the funcitonality.
  - Make any adjustments needed to maintain functionality.
  - Move file.
- Move `Steel-Drum-project.ipynb` from `/Audio/test/` to `/Source/`?
  - Compare this file to the one currently in the root directory.
    - Are they the same or different?
    - Is this the original version?
    - Do we even need to keep this version?
  - If we want to keep this file, we should rename it and movie it.
- Combine the functionalities of `Steel-Drum-project.ipynb` and `sampler.ipynb` into the `metallurgy.py` file.
  - This is a big-ish project. Determine what we need, what to keep, what to toss.
  
## From meeting with George
- Combine files into metallurgy.ipynb
- Test and evaluate different pitch summary methods:
  - Value at onset
  - Average/median for 5ms from onset
  - Average/median from one onset to next onset
- Make more Audio test examples
  - Make MIDI versions
  - Make function to convert MIDI file to numpy array version for comparison
- Longer term project: evaluate pitch detection algorithms on the steelpan
    
## Future plans:
- Machine learning based pitch detection system.
  - The pitch detection algorithms included in Essentia are failing on the test input (which is Twinkle Twinkle Little Star).
  - There is clearly room for improvement in this area.
  - We should devise an ML and/or deep learning based steelpan pitch detection system to test against the Essentia (and/or Librosa?) algorithms.
- Do other awesome work.
