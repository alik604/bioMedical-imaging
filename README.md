# MNIST Brain

> The "[MNIST](http://yann.lecun.com/exdb/mnist/)" of Brain Digits; Given the *brain signal(s)* of **2 seconds each**, captured with the stimulus of **seeing a digit (from 0 to 9)** and thinking about it, determine what the digit is

## Usage

Note that I changed the data location to its dedicated folder, some of the older notebook may require changing the URL 



 ## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

## Inspiration 

//TODO

## Expansion  

//TODO









## Data 

Data is from a single Test Subject [David Vivancos](http://vivancos.com/), and can be found [here](<http://www.mindbigdata.com/opendb/index.html>). 

### **FILE FORMAT**:

The data is stored in a very simple text format including:

**[id]:** a numeric, only for reference purposes.

**[event**] id, a integer, used to distinguish the same event captured at different brain locations, used only by multichannel devices (all except MW).

**[device]:** a 2 character string, to identify the device used to capture the signals, "MW" for MindWave, "EP" for Emotive Epoc, "MU" for Interaxon Muse & "IN" for Emotiv Insight.

**[channel]:** a string, to indentify the 10/20 brain location of the signal, with possible values:
 

|      | **MindWave** | "FP1"                                                        |
| ---- | ------------ | ------------------------------------------------------------ |
|      | **EPOC**     | "AF3, "F7", "F3", "FC5", "T7", "P7", "O1", "O2", "P8", "T8", "FC6", "F4", "F8", "AF4" |
|      | **Muse**     | "TP9,"FP1","FP2", "TP10"                                     |
|      | **Insight**  | "AF3,"AF4","T7","T8","PZ"                                    |



**[code]:** a integer, to indentify the digit been thought/seen, with possible values 0,1,2,3,4,5,6,7,8,9 or -1 for random captured signals not related to any of the digits.

[**size]:** a integer, to identify the size in number of values captured in the 2 seconds of this signal, since the Hz of each device varies, in "theory" the value is close to 512Hz for MW, 128Hz for EP, 220Hz for MU & 128Hz for IN, for each of the 2 seconds.

**[data]:** a coma separated set of numbers, with the time-series amplitude of the signal, each device uses a different precision to identify the electrical potential captured from the brain: integers in the case of MW & MU or real numbers in the case of EP & IN.

There is no headers in the files,  every line is  a signal, and the fields are separated by a tab

For example one line of each device could be (without the headers)

| **[id]** | **[event]** | **[device]** | **[channel]** | **[code]** | **[size]** | **[data]**                                        |
| -------- | ----------- | ------------ | ------------- | ---------- | ---------- | ------------------------------------------------- |
| 27       | 27          | MW           | FP1           | 5          | 952        | 18,12,13,12,5,3,11,23,37,36,26,24,35,42……         |
| 67650    | 67636       | EP           | F7            | 7          | 260        | 4482.564102,4477.435897,4484.102564…….            |
| 978210   | 132693      | MU           | TP10          | 1          | 476        | 506,508,509,501,497,494,497,490,490,493……         |
| 1142043  | 173652      | IN           | AF3           | 0          | 256        | 4259.487179,4237.948717,4247.179487,4242.051282…… |



## About me

> [Directory of repositories](<https://github.com/alik604/ReadMe/blob/master/README.md>)

3rd-year Cognitive science student at Simon Fraser University. Interested in Machine learning, Computational Data science, Finance, Anomaly detection, and Embedded systems for Automation.

Research Interests: Applications of Qualitative Analytics in Human behavior

> ...and Agent behavior, however, that’s just sci-fi... for now. This is useful for side-channel attacks on reinforcement learners 

VP of Cognitive Science Student Society. Member of the Robot Soccer CluSb, and Finance club.



## License

Data is under the *Database Contents License (DbCL) v1.0*

Stuff that is mine to License, and License-able has the [MIT license](https://choosealicense.com/licenses/mit/). 

*if for whatever reason this is inconvenient, fell free to open a **issue** with the reason(s), and i’ll consider changing the License to the **Unlicense*** 
