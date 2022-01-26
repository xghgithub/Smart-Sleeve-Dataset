# Smart-Sleeve Dataset Based on Pressure Mapping Smart Textile

## Description

Pressure mapping smart textile is a new type of sensing modality that transforms the pressure distribution over surfaces into digital "image" and "video", that has rich application scenarios in Human Activity Recognition (HAR), because all human activities are linked with force change over certain surfaces. Based on the pressure mapping smart textile, we have developed Smart-Sleeve. 

We design a Smart-Sleeve using double-sided weft-knitted fabrics. The grey stripes are made of metallic conductive  yarns and the black stripes are made of polymer yarns with carbon powder mixed in, serving as the sensitive layer. The top fabric contains 20 stripes and the bottom one with 10 stripes. Orthogonally stacked together, they form a matrix with 200 sensing points. The size is 40cm x 18cm. To prevent short circuits caused by adjacent sensors touching in a bent arm posture, it is covered with a layer of flexible skin-friendly insulating fabric. The matrix is driving and scanned by a microcontroller. Data is sampled by 12-bits ADCs at 50Hz and transmitted to a smartphone via Bluetooth.

<img src=".\pictures\Smart-Sleeve.png" alt="Smart-Sleeve" width="600" align="middle" />

---

## Data Collection

To evaluate the Smart-Sleeve's ability in recognizing daily activities, we select 18 common activities, 14 healthy subjects (3 females) are invited to participate in the experiment. The participants are all right-handed and therefore wear the sleeve on their right arm. The experiment is divided into 10 rounds, in each round the 18 activities are put into random orders and repeated once. To simulate everyday usage, the smart sleeve is put off and re-worn after each round. 

1. Stand. 
2. Fold arms. 
3. Think. 
4. Side against the wall. 
5. Back against the wall. 
6. Arm on the baffle. 
7. Hug a doll. 
8. Carry a box. 
9. Lean forward at work. 
10. Lean back at work. 
11. Sleep on the table. 
12. Hold cheeks. 
13. Play mobile phone. 
14. Write with a hunchback. 
15. Write with a straight back. 
16. Sit with hands on the armrests. 
17. Sit leaning to the right. 
18. Sit with arms on the legs.


<img src=".\pictures\Activities.png" alt="Activities" width="600" align="middle" />

---

## Data Files

The Smart-Sleeve dataset contains a total of 14 subjects (from "subject_1" to "subject_14"). For each subject, there are 10 folders named "round 1" to "round 10", which contains the data files ("data.csv") and label files ("labels.csv") for each round.

1. data.csv: Each row represents a frame and has 202 numbers. The first number is the timestamp of the lower computer (from the start of the lower computer, the unit is 20ms), and the second number is the timestamp of the upper computer (from 1970/1/1, the unit is 1ms). And the following 200 (20 rows and 10 columns) numbers are the data of the sleeve (we turn the two-dimensional data into one row in row-first order).

1. labels.csv: Each line represents a mark, the first is the index of the posture (see the image above and the activities list), the second is the index of the start-frame, and the third is the index of the end-frame.

---

## Example code

Full disclosure will not be made until after the article is published.

---

## Contributors

Guanghua Xu, Smart-Sleeve development, data collection, and labeling; Wenwu Deng, supporting the hardware development; Jingyuan Cheng, defining research topics, organizing the research team.

---

## Acknowledgements

We would like to express our sincere thanks to Fangting Xie, Ziyu Wu, Mingjie Zhao, and Quan Wan, for their help in the data collection, and to all the volunteers who participated in the experiment.

---

## Funding

Our work is supported "the National Natural Science Foundation of China" (Grant No.62072420) and "the Fundamental Research Funds for the Central Universities" (Grant No.2150110020).


---

Welcome to visit our website: http://pplab.ustc.edu.cn/. If you have any questions about the dataset, please feel free to contact us (xgh@mail.ustc.edu.cn).

