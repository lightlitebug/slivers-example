# Flutter Sliver Example

## (주) pixabay_server.dart의 YOUR_KEY는 pixabay에서 발급받은 key로 바꿔야 합니다.

### sliver는 'a portion of scrollable area'로 정의되어 있습니다. 제 경우는 이 정의가 머리 속에 쏙 들어오지를 않더라고요. 그래서 제 나름대로 sliver를 어떻게 정의를 했냐하면 
- sliver가 a portion of scrollable area라면
- slivers는 scrollable area 자체라고 생각할 수 있기 때문에
- 이제부터는 sliver를 slivers(scrollable area)를 채우는 요소들의 통칭이라고 생각하면 되겠습니다.

### 그러면 sliver는 언제 유용한가? 
- 답은 다양한 위젯들(scroll이 가능한 ListView, GridView 포함)을 scrollable area에 집어넣을 필요가 있을 때 유용합니다.

### Sliver는 다음과 같이 구성되어 있다고 볼 수 있습니다.
- 다양한 위젯들을 scrollable area에 집어 넣기 위한 wrapper widget: CustomScrollview
- 위젯들을 CustomScrollView 의 slivers list property내에 위치
- slivers에 포함되는 위젯들은 sliver 를 aware하는 특수 위젯들로 구성
- SliverAppBar instead of AppBar
- SliverList instead of ListView
- SliverGrid instead of GridView
- SliverToBoxAdapter instead of normal widgets
- SliverFillRemaining - CustomScrollView 내의 빈 공간을 채우고자 할 때

