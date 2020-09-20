



# EEG & BCI related project 

> This repo includes multiple distinct project. 



## BCI 2a

> *4-class motor imagery*

What I did and/or learned

* Added comments as I read and tried to understand the (very) complicated signal processing 
* Tested my [ensemble of ML models](https://github.com/alik604/The-Best-Ensemble) with and without PCA
  * I keep only 2% of the original data and still got extremely competitive results. 
  * without PCA (all data), I outperformed the authors’ Accuracy: 87.9% vs {86.8%, 85%}, Used a `EnsembleVoteClassifier`



## MNIST Brain 

> Mindbigdata, the "[MNIST](http://yann.lecun.com/exdb/mnist/)" of Brain Digits; Given the _brain signal(s)_ of **2 seconds each**, captured with the stimulus of **seeing a digit (from 0 to 9)** and thinking about it, determine what the digit is. [Offical site](http://www.mindbigdata.com/opendb/index.html)

### Discontinuation of work on this project

I really wanted to get this working, I wanted to achieve at least 25% accuracy. 
Unfortunately I have not scene any team or paper achieve more then about 12.5% accuracy. I'm not sure if its even possible to do better. 

* I did learn a lot about Digital signal processing and EEG data. I one attempt, as I recall, I only keep 52hz & 55hz data... a lot better the idiotic approach of blindly throwing LSTMs at the problem.  
* I also learned how to make Bidirectional LSTMs & ConVLSTMs, and combined the two  `Bidirectional(ConVLSTMs(..))` 

* My learning outcome was an increased understanding of sequential models, which I applied to [CMPT 419](https://github.com/alik604/CMPT-419), in which I co-authored ["Predicting the S&P 500 with LTMs and GloVe"](https://github.com/alik604/CMPT-419/blob/master/report.pdf). [Poster](https://github.com/alik604/CMPT-419/blob/master/ML_final_project%20poster.pdf)



## Epileptic Seizure Recognition (EEG)

> This dataset is a pre-processed and re-structured/reshaped version of a very commonly used dataset featuring epileptic seizure detection.

The point of this project was

* Give a sanity test where I was faces with marginal results after 15 hours of attempting *Mindbigdata, the "[MNIST](http://yann.lecun.com/exdb/mnist/)" of Brain Digits*  
  * There was massive code reuse, I just wanted to see if my 3D dataset building and LSTM model was working as intended







## About me

> [Directory of repositories](https://github.com/alik604/ReadMe/blob/master/README.md)

3rd-year Cognitive science student at Simon Fraser University. Interested in Machine learning, Computational Data science, Finance, Anomaly detection, and Embedded systems for Automation.

Research Interests: Applications of Qualitative Analytics in Human behavior

> ...and Agent behavior, however, that’s just sci-fi... for now. This is useful for side-channel attacks on reinforcement learners

(past) VP of Cognitive Science Student Society. Member of the Robot Soccer Club, and Finance club.

## Contributing

Pull requests are welcome.

## License

MNIST brain Data is under the _Database Contents License (DbCL) v1.0_

Stuff that is mine to License, and License-able has the **Unlicense**. Do with my work as you wish.  Internship offers are the recommended attribution :) 
