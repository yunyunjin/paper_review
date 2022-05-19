22.05.17


# Connectivity + Network


## Ismail, L. E., & Karwowski, W. (2020). A graph theory-based modeling of functional connectivity based on eeg: A systematic review in the context of neuroergonomics. IEEE Acess, 8, 155103-155135.
**리뷰논문, 인간 대상, EEG만 사용, 질환 제외하고 건강한 참가자에 대한 실험 연구만, peer-reviewed journals**

### Introduction
---------------------------------------
* functional connectivity is "the statistical interdenpendencies between physiological time series recorded from different brain region
  * 기능적 연결성은 서로 다른 뇌 영역에서 기록된 생리학적 시계열 간의 통계적 상호 의존성임.
*  A considerable amount of work in functional connectivity studies has focused on the blood oxygenation level mainly by functional magnetic resonance imaging (fMRI), due to its good spatial resolution.
   *  기능적 연결성 연구는 주로 우수한 공간 분해능을 가진 fmri연구에서 이루어짐.(혈액 산소 수준에 초점을 맞춤)     
*  However, this technique has low temporal resolution and only provides an indirect measurement of brain activity.To study dynamic cognitive processes and the directional flow of information regarding brain activity, a high temporal resolution technique, such as EEG, enables capturing of the temporal dynamics of brain activity at the sub-second time scale and reflects the rapid changes in neuronal states.
    * 그러나, 이 기술은 낮은 시간 분해능을 가지고 있고 오직 뇌 활동의 간접적인 측정만을 제공함. 뇌 활동과 관련된 동적 인지 과정과 정보의 방향 흐름을 연구하기 위해 EEG와 같은 높은 시간 분해능 기법은 초 미만의 시간 척도에서 뇌 활동의 시간 역학을 포착할 수 있게 하고 신경 상태의 급격한 변화를 반영함.

### Theoretical background
--------------------------
#### funcional connectivity
![list of functional connectivity measurement](https://user-images.githubusercontent.com/102893841/168727972-439284d2-b844-4ba1-ac10-e1219ddd1391.png)

#### Approaches to graph theory
* To study the human brain network on a macroscopic scale, the nodes represent brain regions (i.e., EEG electrodes/sensors), whereas the edges represent statistical measures of association, including anatomical, functional, or effective connections.
  *  거시적 규모로 인간의 뇌 네트워크를 연구하기 위해, node는 뇌 영역을 나타내며, edge는 해부학적, 기능적 또는 효과적인 연결을 포함한 연관성의 통계적 측정을 나타냄
* graph edges include weighted direct, unweighted direct, weighted indirect, and unweighted indirect. A direct edge shows that the information flows in one direction only and that one node’s activity depends on the other (i.e., causal influence); however, an indirect graph shows that information flows in both directions along edges that connect. The weight of the line between two nodes reflects the connectivity strength of the edge, which allows for discrimination between strong and weak connections. Weak connections can be removed by thresholding.
  * edge에는 weighted direct, unweighted direct, weighted indirecr, and unweighted indirect가 있음
  * direct edge는 정보가 한 방향으로만 흐르고 한 node의 활동이 다른 쪽(즉, 인과적 영향)에 의존한다는 것을 보여줌. 
  * 그러나 indirect graph는 정보가 연결된 edge를 따라 양방향으로 흐른다는 것을 보여줌. 
  * 두 node 사이의 선의 무게는 edge의 연결 강도를 반영하므로 강한 연결과 약한 연결을 구별할 수 있음.
  * 약한 연결은 threshold를 통해 제거.

![pipeline](https://user-images.githubusercontent.com/102893841/168746058-e4895eca-db0f-48eb-be39-0a6f78dbadaf.png)


##### Choose a Treshold Value
* Thresholding helps to simplify the complexity of the brain network calculations by eliminating weak, noisy, and insignificant edges from the network.
* Selecting an inappropriate threshold method creates instability and increases the bias; therefore, careful selection is crucial. 
* A key factor is to select a method capable of controlling and minimizing the occurrence of type I errors (i.e., false-positives).
* To perform statistical inference on connectome data, some researchers have suggested to “independently test the hypothesis of interest at each discrete density along the curve”
  *  곡선을 따라 각 이산 밀도에서의 관심 가설을 독립적으로 시험? 이게 몬 말이지
* In contrast, others have recommended more sophisticated methods, such as false discovery rate (FDR) error metric, network-based statistics (NBS), and subnetwork-based analysis.
  * 허위 발견률(FDR) 오류 메트릭스.. NBS 및 하위 네트워크 기반 분석과 같은 방법 제안..?
* A novel methodology, namely the minimum connected component (MCC), has been proposed by Vijayalakshmi et al., which overcomes the threshold issues
  * 최소 연결 구성 요소(Minimum connected component, MCC) 제안 - 문제 극복?

####  GRAPH THEORY MEASURES AND NETWORK TOPOLOGY PROPERTIES

![typical network meausre](https://user-images.githubusercontent.com/102893841/168749333-7fd62e2d-8c3d-406c-b943-8ecbb9cd21d2.png)


### Number of electordes
--------------------------
* large number of electrodes increase the accuracy of eletrical source estimation and signal preprocessing.
* In contrast, some researchers recommened fewer than 32 eletrodes, demonstrating that a small number is adequate to cover the ROI and obtain reliable information.
  *  J. García-Prieto, R. Bajo and E. Pereda, "Efficient computation of functional brain networks: Toward real-time functional connectivity", Frontiers Neuroinf., vol. 11, pp. 1-18, Feb. 2017.
  *  G. Li, Y. Luo, Z. Zhang, Y. Xu, W. Jiao, Y. Jiang, et al., "Effects of mental fatigue on small-world brain functional network organization", Neural Plasticity, vol. 2019, pp. 1-10, Dec. 2019.
  *  F. Wang, X. Zhang, R. Fu and G. Sun, "EEG characteristic analysis of coach bus drivers based on brain connectivity as revealed via a graph theoretical network", RSC Adv., vol. 8, no. 52, pp. 29745-29755, 2018.
*  *S. J. Luck, An Introduction to the Event-Related Potential Technique, Cambridge, MA, USA:MIT Press, 2014.* indicating that the use of 16-32 active eletrodes is better for monitoring brain activity(ERP라서 그런가?)

![number of recording eletrods](https://user-images.githubusercontent.com/102893841/168801065-4182b7b6-eef7-419b-bff6-00f946065e0c.png)



vs code 로 써야지 



