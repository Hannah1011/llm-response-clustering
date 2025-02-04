## 🧑🏻‍💻 LLM Response Clustering Experiments
Open AI embedding 활용해서 쿼리 응답 클러스터링 실험

### 📁 개요
이 레포는 Open AI의 임베딩 데이터를 활용해서 **다양한 클러스터링 기법** 실험하고 비교하기 위해 만들어졌습니다. 
주요 목표는 **유사한 쿼리 응답을 그룹화해서 평가 효율성과 유의미성을 높이는 것**입니다. 

### 📁 진행중인 실험
✔ **K-Means**: 클러스터 개수를 지정한 군집화 (Elbow Method 활용)  
✔ **DBSCAN**: 밀도 기반 클러스터링
✔ **HDBSCAN**: DBSCAN을 개선한 계층적 클러스터링  
✔ **Spectral Clustering**: 비선형 데이터 구조를 반영한 클러스터링  
✔ **차원 축소 기법**: PCA & UMAP  
  → 현 프로젝트에 사용되는 데이터가 비선형적이기 때문에 UMAP을 사용해서 차원 축소 할 예정

### 📁 데이터 및 환경
- **임베딩 데이터**: OpenAI `text-embedding-3-small`  , `text-embedding-3-large`  
- **프로그래밍 언어**: Python 
- **데이터**: 보안을 위해 공개 x

### 📌 실험 결과 정리

✅ **1. K-Means 실험**
- **Elbow Method → 최적 K=10**
 
- **평균 실루엣 점수: 0.17 (낮음)**
- **문제점**:
  - 클러스터 크기가 불균형함.
  - 일부 데이터가 잘못된 클러스터에 배정됨.
  - t-SNE 시각화 결과, 클러스터가 일부 겹침.

✅ **2. UMAP을 활용한 DBSCAN 실험**
- UMAP vs PCA 시각화
  
- **3072D → 50D로 차원 축소 후 클러스터링 진행 중**

✅ **3. HDBSCAN 실험** (tbd)

✅ **4. Spectral Clustering 실험** (tbd)


## 🏗 향후 계획
✔ **DBSCAN/HDBSCAN 최적 파라미터 튜닝**  
✔ **클러스터 품질 평가 (Silhouette Score 분석)**  
✔ **최종적으로 가장 적절한 클러스터링 기법 선정**  

