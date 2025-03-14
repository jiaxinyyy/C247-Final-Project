## UCLA ECE C247 (W25) - Final Project
# Predicting Keystrokes from Electromyography Signals: Exploring Model Architectures and Data Preprocessing
#### Authors:
Megha Maran (megham01@g.ucla.edu), Emily Tang (etangs@ucla.edu), Jiaxin Yang (yangjiaxin0821@g.ucla.edu), and Jinsong Yang (jinsong.yang2000@gmail.com)


### Architectures Explored:
Baseline model comes from the [emg2qwerty](https://github.com/joe-lin-tech/emg2qwerty/tree/main) codebase. All preprocessing steps from the baseline were carried into the new models. A new "time-stretch" augmentation was introduced for comparison. (see branches for different architectures)
- Baseline (TDS-CNN) with preprocessing
- RNN (Current Branch)
- Transformer
- CNN + GRU
- CNN + LSTM

## Best Performing Architecture: CNN + GRU
|Batch|Train/CER|Val/CER|Test/CER|
|----------|-----------|-----------|-----------|
| 10 | 17.65618  | 17.65618  | 17.80851  |
| 32 | 23.57111  | 23.57111  | 23.2980   |
---

## Note on .gitignore
- Data can be downloaded [here](https://ucla.app.box.com/s/e54bnjvy6hl33ao3jhvz7711q5iwkws5)
- All logs saved to /logs will not be stored in repository
