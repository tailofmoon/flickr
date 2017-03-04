# flickr
flickr app

## Intro
Using Flickr API you can retrieve a plethora of photographs and in turn, may create awesome applications. Moreover, you may upload your application to Flickr's marketplace APP Garden and make bucks and recognition too.


## API 키 얻기
Flickr에서 API 키를 얻어야합니다. flickr.com에 로그인하려면 Yahoo! 계정이 있어야하며,없는 경우 Flickr에 가입해야합니다. Flickr 내에서 브라우저를 https://www.flickr.com/services/api/ 로 지정하십시오. API 키를 작성하려면 'APP 작성'으로 이동하십시오. 'API 키 요청'링크를 클릭하십시오.


## 앱 개요
이 응용 프로그램에서는 Flickr에서 최신 사진 10 장을 가져옵니다.


## 메소드 이해하기
Flickr API의 메소드는 XML 또는 JSON 형식의 데이터를 반환하는 끝점 (URL)을 구성합니다. 이 작업이 완료되면 많은 프로그래밍 언어를 사용하여 해당 데이터를 디코딩하여 사용자에게 제공 할 수 있습니다. 모든 Flickr API 메소드에는 몇 가지 인수가 전달됩니다. 일부는 필수이고 일부는 선택적입니다.

flickr.photos.getRecent를 클릭하면 https://www.flickr.com/services/api/flickr.photos.getRecent.html 로 이동합니다. 메소드에 대한 문서는 여기에서 볼 수 있습니다. 이 메소드에는 네 가지 유형의 인수를 사용할 수 있음을 알 수 있습니다. 그 중 'api_key'가 필요합니다.

많은 옵션 인자를 'extra'로 전달하여 description, license, date_upload, date_taken, owner_name 등의 유용한 정보를 반환 할 수 있습니다.

'per_page 또 다른 선택적 인수는 페이지 당 리턴 할 사진 수를 리턴합니다.이 인수가 제공되지 않으면 기본적으로 백 개의 사진이 리턴됩니다.

결과가 포함 된 페이지 수를 반환하려면 다른 선택적 인수 'page'를 사용할 수 있습니다. 사용하지 않으면 결과의 단일 페이지 만 반환됩니다.


## URL의 구조
URL을 이해하는 데 약간의 시간을 투자하면 양식을 이해하는 데 도움이되며 URL을 수정하고 수정할 수 있습니다.

URL은 다음과 같습니다. https://api.flickr.com/services/rest/?method=flickr.photos.getRecent&api_key=your_key&per_page=10&format=json&nojsoncallback=1

Sp URL은 https://api.flickr.com/services/rest/?로 시작합니다. FLick'r API는 SSL (Secure Socket Layer)이없는 http를 지원하지 않으므로이 URL을 실행하는 서버에서 https를 사용하도록 설정해야합니다. 그런 다음 method 키워드는 사용하려는 메소드를 추가합니다.이 경우 'flickr.photos.getRecent'입니다. '&'는 URL의 다음 부분을 추가하는 데 사용됩니다. 여기서 'api_key'를 제공해야합니다. 그런 다음 'format = json'으로 지정됩니다. 즉, JSON 형식을 사용하고 'nojsoncallback = 1'은 래퍼 기능이없는 원시 JSON을 지정합니다. 대신 콜백 함수를 사용하려면 'jsoncallback = name_of_your_callback_function'을 사용할 수 있습니다.

'flickr.photos.getSizes'메서드의 경우에도 비슷한 방식으로 URL을 생성합니다.


## 프로그래밍 및 데이터 
URL 요청한 데이터를 JSON 데이터로 디코딩하고 이를 사용자에게 제공해야합니다. 'https://www.flickr.com/services/api/' 페이지는 'API 키트'섹션의 프로그래밍 언어 사용 목록을 제공합니다. 이 애플리케이션의 경우 Jquery를 사용하여 반환 된 JSON 데이터를 디코딩 한 다음 HTML 페이지에 추가합니다.




