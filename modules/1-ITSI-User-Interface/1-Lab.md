이 모듈에서는 데모 환경에 로그인하여 ITSI 의 UI 를 탐색합니다.

---

# Task 1 : 데모 환경에 로그인하기

# Task 2 : Service Analyzer 와 연관된 뷰를 탐색하기

1. **ITSI > Service Analyzer** 메뉴로 이동하여 (Demo)- Buttercup Retail 의 서비스 분석기가 뜨는 것을 확인합니다
2. 오른쪽 상단의 _tree view_ 아이콘을 클릭하여 서비스간의 종속관계 구성을 볼 수 있도록 합니다

   ![](../../src/images/1-2-tree-view.jpg)

3. 노란색으로 표시되는 **_Buttercut checkout_** 서비스를 **클릭**합니다. 그러면 사이드패널이 열리고 API와 주요 에피소드에 대한 정보가 표시됩니다.

   - 클릭하면 _Buttercut checkout_ 동그라미가 하이라이트 되고 화면의 중앙으로 이동합니다. 오른쪽에 KPI의 목록이 표시되는 것을 확인 할 수 있습니다.

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
9. KPI 리스트 창에서 **_CPU Utilization: %_** KPI를 클릭합니다
