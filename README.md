# Android-trafficdetection-using-Linear-Regression
1	Introduction

The dominant market position of Android OS has also attracted the interest of malware authors exploring the vulnerabilities of Android OS. As per G DATA mobile malware report [1], their experts have discovered around 4900 fresh Android malware every day in the first quarter of 2015. Malware have been categorized based on the functionalities of their malicious payload as license esca- lation, remote control by communicating with C & C ser- ver, financial charge and collecting information [2]. The scale of damage caused by an Android malware depends on its functionality and sometimes the results of its activity are invisible for the users which are a cause of concern. AVG mobile security team [3] recently discovered an Android malware, PowerOffHijack, which hijacks the shutdown process and the device remains functional giving it the freedom to move around on the device and steal data even though it appears to be off. In 2014, Doctor Web [4] had issued a warning to Android users about a new Trojan (BankBot.21.origin) that can steal information about the credit cards they use for transactions on Google Play. With such sophistication and experimentation, Android malware has become a critical threat.
This has led to an increase in the research work in the area of Android malware detection where researchers have introduced novel techniques and improvised the current ones focusing on Android malware detection.
In this paper, we have presented various detection techniques which give a better understanding of these techniques and explore the fact that detecting known/un- known malware using machine learning techniques is on the rise. An updated image of the past and latest Android malware detection techniques is discussed in this paper, and illustrated with examples.
 

 
This paper is structured as follows. In Sect. 2, we dis- cuss Android Architecture and Sect. 3 presents the com- ponents of an Android application. Section 4 provides an overview of the security features present in Android. Sec- tion 5 presents various Android application analysis methods and Sect. 6 presents the Android malware detec- tion techniques. Section 7 presents various Android mal- ware detection systems that have been developed. Emerging directions are discussed in Sect. 8 and finally, we conclude in Sect. 9.

2 Android malware detection techniques

A malware detector identifies and contains malware before it can reach a system or network [10]. This section intro- duces the commonly used Android malware detection techniques and their evaluation criteria. Before proceeding further, let us briefly discuss what Machine learning is and how it is categorized.
Machine learning [11] is the study of computer pro- grams capable of learning their own previous experience to improve their performance of a task. Machine learning has been used widely in the field of Android malware detection to either learn malicious characteristics to detect malware based on the similarity (misuse detection) with them or learn from the benign characteristics to detect malware based on the deviation from them (anomaly detection) [12]. Machine learning algorithms can be segregated into two categories (Fig. 2)—supervised and unsupervised learning. Supervised learning is inferring a function from labeled data for classifying data for responses that have few known values or for performing regression for responses that are continuous and real-valued. Unsupervised learning is exploring the data to find some intrinsic structures in them such as clustering data to find similarity group called clusters.
This technique detects malware by comparing them with the knowledge accumulated from known malware in the form of their signatures. Malware is detected based on the similarity with the known malware. It can accurately detect known malware but is quite ineffective against unknown attacks as no signatures are available. Also, variants of the previous malwares that deviates slightly are difficult to be detected by this technique. To overcome this restriction, machine learning has been used in misuse detection to automatically generate signatures for detecting unknown malwares [17]. Misuse detection requires continuous updation of the signature database with the signatures of the known malware. Another problem is that with such large increase in the number of malwares which have been detected [1], the size of the signature databases has also  increased which makes it not feasible to be stored on the mobile phones being constrained by limited storage [15].

3 Anomaly detection

It is considered complementary to misuse detection. It focuses on the normal behavior of an Android application rather than detecting the presence of malware signatures. Malware is detected based on the deviation from the normal behavior. Machine learning has also been used in anomaly detection which is characterized by two phases—training phase and a detection phase. In training phase, the normal
 
behavior of Android applications is learned using machine learning and then during detection phase, the learned normal behavior is compared with the current behavior of an Android application being analyzed for classification as malicious or benign or in other words malware detection. Since this technique does not rely on the characteristics of known malware, it can detect novel ones since similar behavior patterns are shared by novel and existing malware because novel malwares are often created by adding new malicious behaviors to the existing malware [18]. However, any previously unobserved normal behavior can also be flagged as malicious by this technique resulting in false alarms. To reduce the false alarms, specification-based detection is performed in which specifications of Android applications are manually developed and then detection is performed based on the deviations from normal specifica- tions of an Android application. The disadvantage of this technique is that developing the specifications of Android applications is a very time-consuming process [15].
For the evaluation of the efficiency of these techniques following parameters are highlighted in [16, 19] in the context of intrusion-detection systems:
•	Accuracy—It’s a measure of correctness. Inaccuracy occurs when a legitimate application is flagged as malicious i.e., false positive.
•	Performance—It’s the rate at which the applications are analyzed for malware detection by a malware detector. Low rate implies compromising real-time detection.
•	Completeness—It’s the capability of a detector to  detect all the malicious applications. Incompleteness occurs when a malicious application is flagged as legitimate i.e., false negative.
•	Fault Tolerance—The malware detector itself should be resilient to malicious attacks. Being vulnerable to such attacks would defeat the whole purpose of the malware detection.
•	Timeliness—Timely detection of a malware will not only help in preventing the damage caused but also curb its propagation. ESET, an IT security firm [20] recently detected a malware Android/Spy.Feabme.A which steals facebook credentials. This malicious application was installed by over 500,000 Android users from Google play store and following its detec- tion it was taken down. This fact highlights the timely detection of malware and prevention of its propagation.

4 Conclusion

A lot of work has been done in the area of Android mal- ware detection. Researchers are also using the combination of misuse and anomaly detection for improving the detection accuracy. This paper lists the features extracted for the purpose malware detection as well as various machine learning algorithms being used for the same. The presence of machine learning algorithms in all categories of malware detection techniques and analysis methods highlights the fact that machine learning algorithms are being used frequently in this area for detecting Android malware in the wild.
  
References

1.	G Data Mobile Malware Report (2015) https://public.gdatasoftware. com/Presse/Publikationen/Malware_Reports/G_DATA_Mobile MWR_Q1_2015_US.pdf
2.	Zhou Y, Jiang X (2012) Dissecting Android malware: charac- terization and evolution. Proc IEEE Symp Secur Priv 4:95–109
3.	‘‘AVG.’’ http://now.avg.com/malware-is-still-spying-on-you-after- your-mobile-is-off/
4.	‘‘Dr. Web.’’ https://news.drweb.com/show/?i=5860&lng=en
5.	‘‘Platform Architecture.’’ https://developer.android.com/guide/ platform/index.html
6.	‘‘ART and Dalvik.’’ https://source.android.com/devices/tech/ dalvik/
7.	‘‘Android Studio.’’ https://developer.android.com/studio/index. html
8.	‘‘Application Fundamentals.’’ https://developer.android.com/ guide/components/fundamentals.html
9.	Enck W, Ongtang M, McDaniel P (2009) Understanding Android Security. IEEE Secur Priv 7:50–57
10.	Christodorescu M, Jha S (2004) Testing malware detectors. ACM SIGSOFT Softw Eng Notes 29:34
11.	Mitchell TM (1997) Machine learning. McGraw-Hill, Inc., New York
12.	Sammut C, Webb GI (2011) Encyclopedia of machine learning. Springer Sci. Bus. Media, vol. 33, pp. 439–447
13.	Kotsiantis SB (2007) Supervised machine learning: a review of classification techniques. Mach Learn 31:249–268
14.	Ghahramani Z (2004) Unsupervised learning. Mach. Learn. 2003 (Summer Sch., pp 72–112
15.	Ning P (2003) Intrusion detection techniques. Internet Encycl
16.	Debar H, Dacier M, Wespi A (1999) Towards a taxonomy of intrusion-detection systems. Comput Netw 31(8):805–822
17.	Hassan D, Might M (2014) A similarity-based machine learning approach for detecting adversarial android malware
18.	Christodorescu M, Jha S, Seshia SA, Song D, Bryant RE (2005) Semantics-aware malware detection. In: Proceedings of IEEE symposium security privacy, pp 32–46
19.	Porras PA, Valdes A (1998) Live traffic analysis of TCP/IP Gateways. In: Proceedings of 1998 ISOC symposium network distributed system security NDSS98
20. ‘‘ESET.’’
21.	Bla¨sing  T,  Batyuk  L,  Schmidt  AD,  Camtepe  SA,  Albayrak  S (2010) An android application sandbox system for suspicious software detection. In: Proceedings of 5th IEEE international conference malicious unwanted software, Malware 2010, pp 55–62
22.	Almin SB, Chatterjee M (2015) A novel approach to detect android malware. Procedia Comput Sci 45:407–417
23.	Shabtai A, Kanonov U, Elovici Y, Glezer C, Weiss Y (2012) ‘Andromaly’: a behavioral malware detection framework for android devices. J Intell Inf Syst 38(1):161–190

