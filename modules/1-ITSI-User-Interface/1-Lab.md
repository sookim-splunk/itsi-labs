이 모듈에서는 데모 환경에 로그인하여 ITSI 의 UI 를 탐색합니다.

- [Task 1 : 데모 환경에 로그인하기](#task-1--데모-환경에-로그인하기)
- [Task 2 : Service Analyzer 와 연관된 뷰를 탐색하기](#task-2--service-analyzer-와-연관된-뷰를-탐색하기)
- [Task 3 : Service Analyzer 뷰를 필터하고 새로 저장하기](#task-3--service-analyzer-뷰를-필터하고-새로-저장하기)
- [Task 4 : Deep Dive로 심각도에 따른 잠재 이슈를 살펴보기](#task-4--deep-dive로-심각도에-따른-잠재-이슈를-살펴보기)
- [Task 5 : 서비스 헬스 스코어와 잠재 원인을 예측해보기](#task-5--서비스-헬스-스코어와-잠재-원인을-예측해보기)
- [Task 6 : ITSI 의 기반이 되는 데이터 찾아보기](#task-6--itsi-의-기반이-되는-데이터-찾아보기)

---

# Task 1 : 데모 환경에 로그인하기

# Task 2 : Service Analyzer 와 연관된 뷰를 탐색하기

1. **ITSI > Service Analyzer** 메뉴로 이동하여 (Demo)- Buttercup Retail 의 서비스 분석기가 뜨는 것을 확인합니다
2. 오른쪽 상단의 _tree view_ 아이콘을 클릭하여 서비스간의 종속관계 구성을 볼 수 있도록 합니다

   ![](../../src/images/1-2-tree-view.jpg)

3. 노란색으로 표시되는 **_Buttercup checkout_** 서비스를 **클릭**합니다. 그러면 사이드패널이 열리고 API와 주요 에피소드에 대한 정보가 표시됩니다.

   - 클릭하면 _Buttercup checkout_ 동그라미가 하이라이트 되고 화면의 중앙으로 이동합니다. 오른쪽에 KPI의 목록이 표시되는 것을 확인 할 수 있습니다.

4. **_Open all in Deep Dive_** 를 **클릭**하여 deep dive 화면에서 KPI를 모두 리스트합니다

   - 새로운 탭으로 창이 열립니다. 각 레인에 마우스를 올려놓아보고, 저장한다면 해당 화면을 나중에 다시 리뷰 할 수 있습니다

5. 다시 **Service Analyzer** 로 돌아와서 KPI 창의 하단에 Event Analytics 부분에 내용이 있는지 확인합니다. **_Critical and High Episodes_** 라는 항목이 볼드 처리 되어있습니다.

   > [!Warning]
   > 이 단계에서는 모든 에피소드에 대해 acknowledge 를 클릭하지 마세요

6. 바로 오른쪽에 있는 **_View All_** 버튼을 **클릭** 하여 크리티컬이거나 high 심각도의 에피소드를 확인합니다

   - Alerts and Episode 화면이 새로운 탭으로 창이 열립니다.

7. 화면 하단에 있는 리스트에서 에피소드 하나를 클릭하여 더 많은 정보와 옵션을 확인합니다.

   - 다음 모듈에서 Acknowledge를 클릭하게되면 해당 에피소드의 오너십을 설정하고 문제해결을 시작합니다
   - **해당 모듈에서는 아무것도 클릭하지 않습니다**

8. **Episode Review** 창을 닫고 **Service Analyzer** 로 돌아갑니다
9. KPI 리스트 창에서 **_RUM: Interaction Count_** KPI를 클릭합니다

   - 이 KPI 와 연결된 엔티티를 표시하는 추가 패널이 열립니다

10. **_APM: Rate_** KPI를 클릭해봅니다
11. **_APM: Rate_** KPI의 오른쪽 그래프라인에 마우스를 호버하여 임계값이 어떻게 변해왔는지를 확인하고, 해당 KPI의 심각도 (severity) 를 함께 확인합니다
12. 오른쪽에 표시되는 엔티티 이름을 클릭합니다
13. 특정 엔티티 하나가 어떤 성능을 보이는지 확인할 수 있는 새 탭이 열립니다.
14. **Service Analyzer**로 다시 돌아옵니다

# Task 3 : Service Analyzer 뷰를 필터하고 새로 저장하기

1. **Service Analyzer > Analyzers** 화면에서 우측 상단의 [Create Service Analyzer] 버튼을 클릭하여 새로운 서비스 분석기를 정의합니다
   - Name : Buttercup All Services
   - Permissions : Private
2. 리스트에서 방금 만든 서비스 분석기 이름을 눌러 화면으로 이동합니다
   - 현재는 아무 필터도 걸려있지 않기 때문에 모든 서비스가 표현됩니다.
3. 좌측 상단의 **Filter services** 필드에서 **_Buttercup Retail_** 서비스명을 필터 해 줍니다
4. **Show service dependencies** 를 체크하여 모든 서비스 타일이 표현되도록 합니다
5. 우측 상단에 [Save] 버튼을 눌러 변경사항을 저장합니다

# Task 4 : Deep Dive로 심각도에 따른 잠재 이슈를 살펴보기

1. 아래쪽의 KPI 타일에서 노란색이거나 더 심각한 KPI 타일에 마우스를 올려놓아봅니다
   - 타일의 오른쪽 위에 체크마크가 보이죠?
2. 심각해보이는 KPI 중 **Disk Space Used %** 타일을 클릭 해 봅니다
3. 오른쪽에 뜨는 KPI 패널에서 **Open all in Deep Dive** 를 클릭하여 딥다이브 새 창으로 이동합니다
   - 그러면 선택한 KPI에 대한 레인으로만 구성된 Deep Dive 창이 자동으로 구성됩니다. 시간에 따라 모든 KPI가 어떻게 변화하는지를 확인 할 수 있습니다. 자세한 내용은 다른 모듈에서 확인 하겠습니다

# Task 5 : 서비스 헬스 스코어와 잠재 원인을 예측해보기

1. ITSI 에서 **Dashboards > Predictive Analytics** 메뉴로 이동합니다
2. **Service** 드롭다운에서 _Buttercup Retail_ 을 선택합니다
3. Model 드롭다운에서 사전에 학습 된 트레이닝 모델을 선택해야하지만, 현재 랩 환경에서는 트레이닝 된 모델이 없습니다.

# Task 6 : ITSI 의 기반이 되는 데이터 찾아보기

1. ITSI 에서 **Search** 메뉴로 이동합니다
2. How to Search 박스 아래에 표시되는 버튼 중 [Data Summary] 버튼을 클릭합니다
3. 표시되는 팝업에서 리스트되는 호스트, 소스, 소스타입 등으로 통해 어떤 데이터들이 인덱스 되고 있는지를 파악 해 봅니다
4. 창을 닫고 서치바에 아래와 같은 조건으로 검색 해 봅니다

   - index=itsi_summary
   - last 60 minutes

   > [!Note]
   > 이 인덱스는 KPI 검색 결과를 저장합니다. 이러한 각 이벤트는 현 시점의 하나의 KPI를 나타내며 각 서비스에 대한 Service Health event 내용도 있습니다. 관련성이 높은 필드인 alert_level, alert_severity, entity_title 등을 살펴보세요

5. 서치바에 아래와 같은 조건으로 검색 해 봅니다

   - index=itsi_tracked_alerts
   - last 60 minutes

   > [!Note]
   > 이 인덱스에는 노터블 이벤트가 저장됩니다. source (correlation search name), alert_level, alert_value, entity_title, kpi, owner, status 같은 주요 필드들을 한번 살펴보세요
