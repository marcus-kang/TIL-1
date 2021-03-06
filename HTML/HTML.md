# HTML관련 TIL
## 20190121 TIL

* 브라우저는 다른 HTML 요소와는 조금 다른 식으로 img 요소를 처리함<br>
HTML 페이지를 읽고 난 후 웹 서버로부터 각 이미지를 회수한 뒤 보여줌<br>
만약 웹페이지에 큰 이미지가 한 개 이상 있다면 섬네일(큰이미지를 보기 위해 사용자들이 클릭할 수 있는 작은 이미지)을 생성하여 웹 페이지를 좀 더 유용하게 하고 내려받는 속도를 빠르게 할 수 있음

* 웹 브라우저가 널리 지원하는 이미지의 형식으로는 JPEG, PNG, GIF가 있고 JPEG 형식은 사진이나 다른 복잡한 이미지에 적합<br>
  GIF나 PNG형식은 로고나 단색으로 구성된 간단한 그래픽과 선, 텍스트에 적합<br>
  JPEG 이미지는 다양한 품질로 압축될 수 있고 필요한 정도에 따라 파일 크기와 품질 사이에 최적의 균형을 맞추어서 사용하길 권장<br>
  GIF & PNG는 무손실 형식이고 이는 파일크기가 JPEG보다 크다는 것을 의미, PNG는 GIF보다 투명도를 처리하는 데 더 낫고 256색으로 한정된 GIF보다 더 많은 색을 가지고 있음 
  GIF만 유일하게 애니메이션 지원<br>
* img element의 alt속성은 이미지에 대한 설명을 나타날 때 사용, ex) <img src="banana.png" alt="바나나"> 이런식으로 사용하고 해당 이미지가 표시되지 않는 경우 alt에 있는 내용이 표시됨, 또한 시각장애인을 위해 이미지를 설명하는 스크린 리더기에서도 <br>

* a태그에 주로 사용되는 title 속성은 해당 element에 대한 설명을 툴팁형식으로 보여줌(head안의 title과 혼동하면 안됨) ex) <a href="#" title="링크예제설명입니다.">링크예제</a>, a태그가 아닌 다른 element에도 사용은 가능하지만 많이 쓰이지 않음<br>

* 인용구를 지원하는 태그<br>
짧은 인용구: q태그(문단 안에서 인용할 때 사용하는 인라인 요소)  ==> <q>이몸이 죽고죽어 일백번 고쳐죽어..</q><br>
그냥 "" 큰 타옴표를 사용하는것보다 좀 더 구조적이고 의미있게 하기위한 것(브라우저에게 실제 인용구라는 것을 인식하게 하기 위함)<br>
긴 인용구: blockquote태그(항상 앞과 뒤에 라인브레이크를 가진 것처럼 표시되는 블록요소) ↓
<blockquote>이 몸이 죽고 죽어 일백 번 고쳐죽어, 백골이 진토 되어 넋이라도 있고 없고 임 향한 일편단심이야 가실 줄이 있으랴</blockquote>
<hr>
<h1>20190123 TIL</h1> <br>
<h2>html5에서 추가된 새 요소중 중요한 요소</h2> <br>
article: 블로그 포스트, 사용자 포럼, 신문기사처럼 페이지에 있는 독립적인 콘텐츠를 표현 <br>
nav:     페이지에서 내비게이션 링크를 의미하는 콘텐츠를 포함 <br>
header:  페이지 상단이나, 페이지의 한 구간의 상단에 있는 콘텐츠 <br>
footer:  페이지 하단, 혹은 한 구간의 하단에 있는 콘텐츠 <br>
aside:   설명메모나 사이드바처럼, 페이지 콘텐츠에 대한 보충정보를 나타내는 콘텐츠를 포함 <br>
section: 보통 header나 footer와 함께 주제별로 콘텐츠를 모아 놓은 것 <br>
time:    날짜나 시간, 혹은 이 둘 모두를 포함 <br>
video:   페이지에 비디오 미디어를 추가할 때 사용 <br>
<strong>section과 article이 햇갈릴 수 있는데 관련된 콘텐츠를 묶을 때는 section을, 뉴스기사나 블로그 포스트, 간략한 보고서 같은 독립적인 정보의 콘텐츠를 묶을 때는 article을 사용하는 걸 권장</strong> <br>
<hr> <br>
<h1>20190124 TIL</h1>
<h2>video 요소</h2><br>
페이지에 동영상 콘텐츠를 추가할 때 사용되며 사용방법은 <br>
video controls autoplay width="512" height="288" src="video/test.mp4" <br>
<strong>속성</strong> <br>
- controls: 비디오와 오디오 재생을 조정하는 컨트롤을 제공(브라우저에 따라 다름)<br>
- autoplay: 속성명에서도 유추 가능하듯 이 속성 명시할 경우 페이지가 뜨자마자 동영상이 자동 재생됨 <br>
- poster: 비디오가 시작되지 않을 경우 포스터 이미지를 보여줄 수 있음, img요소의 alt와 비슷한 역할<br>
- id: 아이디 추가해서 스타일 가미 가능 <br>
- src: img요소의 src와 흡사한데, 비디오 파일 원본의 위치가 담긴 url을 설정 <br>
- preload: 보통 최적화를 목적으로 비디오를 어떤 식으로 가져올지 제어하는 세밀한 컨트롤에 사용됨 <br>
- loop: boolean 속성으로 재생이 끝난 후 비디오를 자동으로 재시작하는 기능을 수행 <br>
- width, height: 비디오 재생영역(일명 뷰포트)의 너비와 높이를 결정, poster 속성을 사용하고 있다면 포스터 이미지 크기도 이 너비와 높이에 맞춰짐<br>
비디오 역시 크기가 조정되는데, 영상 비율(4:3 혹은16:9)로 맞춰지므로 좌우 또는 상하에 공간이 생길 것이며, 비디오는 편지함이나 기념품 상자 모양으로 재생 영역 크기에 맞춰질 것임, 최상의 성능과 화질로 보여주길 원하면 비디오의 원본 영역에 맞추길 권장 <br>
- source: 브라우저마다 비디오 지원 형식이 다르므로 src속성 하나만으로 모든 브라우저를 다 지원할 수 없음, 각각의 브라우저에서 동영상을 지원하기 위해 각각의 포맷을 설정하는 속성(쉽게 얘기해 미디어를 여러개 설정할 때 사용하는 요소정도로 이해) <br>
참조 url: https://developer.mozilla.org/ko/docs/Web/HTML/Element/Video <br>
<p></p>
<strong>HTML5에서 추가된 form 요소</strong> <br>
숫자입력: input type="number" <br>
범위입력: input type="range" min="0" max="5" step="5" <br>
색상입력: input type="color" <br>
날짜입력: input type="date" <br>
이메일입력: input type="email" <br>
전화번호 입력: input type="tel" <br>
url 입력: input type="url" <br>
<h3>위의 요소들을 데스크톱 브라우저에서는 차이점을 못 느낄지 모르지만, 모바일 브라우저에서는 /나 @처럼 필요한 문자를 쉽게 입력할 수 있는 맞춤형 키보드가 표시된다고 함<br>
모든 브라우저가 이런 입력 유형을 지원하지는 않아서 제대로 보이지 않는 것도 있을 수 있음</h3> <br>
<p>
form요소의 name 속성 작동방식 <br>
클라이언트에서 폼에 데이터 입력 후 전송 => 브라우저는 폼의 데이터와 유일한 이름을 사용하는 name속성을 묶어서 포장 후 서버로 전송 <br>
<strong>ex) zip이라는 name의 input요소에 우편번호로 10000을 입력 하면, 브라우저는 폼이 전송될 때 zip=10000을 서버로 보냄</strong> <br>
<hr>
<h1>20190125 TIL</h1> <br>
html의 form이 더 커지기 시작하면 요소를 시각적으로 묶는 것이 도움이 되는데 이때 사용하는 것이 fieldset과 legend요소임 <br>
field요소는 input요소의 세트를 둘러싸고, legend는 input 그룹에 대한 라벨을 제공 <br>
<img src="https://user-images.githubusercontent.com/44331989/51725246-8d5e3e80-20a4-11e9-88d5-da20eb499d21.JPG"> 
결과: <img src="https://user-images.githubusercontent.com/44331989/51725340-f3e35c80-20a4-11e9-841e-474a06d36cd3.JPG"> <br>

selectbox에서 다중 선택이 필요할 경우 select 태그에 multiple을 추가하면 됨 <br>
해당 필드를 필수입력으로 해야 할 경우 태그에 required을 추가하면 됨 <br>
<h3>html은 플러그인 없이도 audio요소를 사용해 페이지에서 오디오를 재생하는 표준방법을 제공하고 있음</h3>
사용방법은 video요소와 매우 흡사함 <br>
audio src="songs/최재훈-비의랩소디.mp3" id="boombox" controls(볼륨 조절, 구간 조절 컨트롤), 단 video요소와 마찬가지로 브라우저 종류에 따라 재생 컨트롤 모양은 가지각색임 <br>
비디오처럼 오디오에 대한 표준 인코딩은 존재하지 않으며 유명한 형식으로는 mp3, wav, Ogg Vorbis가 있고 현재시점에 위 세가지 형식 모두를 지원하는 유일한 브라우저는 크롬이라고 함 <br>audio요소와 이 요소의 javascript API는 많은 컨트롤을 제공한다고 함<br>
<h1>20190129 TIL</h1>	
<h2>Ul li 가로로 정렬하는 방법<h2> 
참조 url: http://www.acidzazz.com/2013/03/ul-li.html 
li에 float:left를 추가, ul을 li의 height만큼 늘어나게 하려면 ul의 overflow:auto 추가 <br>
  
  
  





<p><br>  
<p><br>
<p><br>
  <strong>출처: Head First HTML and CSS(개정판)</strong>


