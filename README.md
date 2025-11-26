# opensouce-project
# top(탑)

### **top**  명령어는 현재 OS의 상태를 나타내주는 CLI 어플리케이션입니다.


###### 메모리 사용량, CPU 사용량 등을 나타내주며 top를 실행하는 동안에는 주기적인 업데이트로 실시간에 근접한 내용을 보여줍니다. 리눅스에서 top 명령어를 실행하면 아래와 깉이 노출됩니다. 위에는 전체의 요약이 있으며 아래에는 각 프로세스마다 구체적인 내용을 포함하고 있습니다.
![image](<!DOCTYPE html>
<html lang="ko">

                                                                <head>
                <script type="text/javascript">if (!window.T) { window.T = {} }
window.T.config = {"TOP_SSL_URL":"https://www.tistory.com","PREVIEW":false,"ROLE":"guest","PREV_PAGE":"","NEXT_PAGE":"","BLOG":{"id":296044,"name":"morenice","title":"morenice's blog","isDormancy":false,"nickName":"morenice","status":"open","profileStatus":"normal"},"NEED_COMMENT_LOGIN":false,"COMMENT_LOGIN_CONFIRM_MESSAGE":"","LOGIN_URL":"https://www.tistory.com/auth/login/?redirectUrl=https://www.morenice.kr/30","DEFAULT_URL":"https://www.morenice.kr","USER":{"name":null,"homepage":null,"id":0,"profileImage":null},"SUBSCRIPTION":{"status":"none","isConnected":false,"isPending":false,"isWait":false,"isProcessing":false,"isNone":true},"IS_LOGIN":false,"HAS_BLOG":false,"IS_SUPPORT":false,"IS_SCRAPABLE":false,"TOP_URL":"http://www.tistory.com","JOIN_URL":"https://www.tistory.com/member/join","PHASE":"prod","ROLE_GROUP":"visitor"};
window.T.entryInfo = {"entryId":30,"isAuthor":false,"categoryId":515509,"categoryLabel":"IT/DevOps"};
window.appInfo = {"domain":"tistory.com","topUrl":"https://www.tistory.com","loginUrl":"https://www.tistory.com/auth/login","logoutUrl":"https://www.tistory.com/auth/logout"};
window.initData = {};

window.TistoryBlog = {
    basePath: "",
    url: "https://www.morenice.kr",
    tistoryUrl: "https://morenice.tistory.com",
    manageUrl: "https://morenice.tistory.com/manage",
    token: "9RiCEC8ko34fP6dT+nra9Rj1NV1apGSDJh8xTNB7TM39mPpmsmt595DxTqOFJvqo"
};
var servicePath = "";
var blogURL = "";</script>

                
                
                        <!-- BusinessLicenseInfo - START -->
        
            <link href="https://tistory1.daumcdn.net/tistory_admin/userblog/userblog-b01726c8aeb47bdb6a378467404d8bd37fde5262/static/plugin/BusinessLicenseInfo/style.css" rel="stylesheet" type="text/css"/>

            <script>function switchFold(entryId) {
    var businessLayer = document.getElementById("businessInfoLayer_" + entryId);

    if (businessLayer) {
        if (businessLayer.className.indexOf("unfold_license") > 0) {
            businessLayer.className = "business_license_layer";
        } else {
            businessLayer.className = "business_license_layer unfold_license";
        }
    }
}
</script>

        
        <!-- BusinessLicenseInfo - END -->
        <!-- GoogleAnalytics - START -->
        <script src="https://www.googletagmanager.com/gtag/js?id=G-FRCPGCSJW2" async="async"></script>
<script>window.dataLayer = window.dataLayer || [];
function gtag(){dataLayer.push(arguments);}
gtag('js', new Date());
gtag('config','G-FRCPGCSJW2', {
    cookie_domain: 'morenice.tistory.com',
    cookie_flags: 'max-age=0;domain=.tistory.com',
    cookie_expires: 7 * 24 * 60 * 60 // 7 days, in seconds
});</script>

        <!-- GoogleAnalytics - END -->

<!-- System - START -->
<script src="//pagead2.googlesyndication.com/pagead/js/adsbygoogle.js" async="async" data-ad-host="ca-host-pub-9691043933427338" data-ad-client="ca-pub-8136595379682794"></script>
<!-- System - END -->

        <!-- GoogleSearchConsole - START -->
        
<!-- BEGIN GOOGLE_SITE_VERIFICATION -->
<meta name="google-site-verification" content="gmxAGOBpphEkC0ZbXr_Wq_iZ8aKg7ceAJjCkw4ccQOs"/>
<!-- END GOOGLE_SITE_VERIFICATION -->

        <!-- GoogleSearchConsole - END -->

        <!-- TistoryProfileLayer - START -->
        <link href="https://tistory1.daumcdn.net/tistory_admin/userblog/userblog-b01726c8aeb47bdb6a378467404d8bd37fde5262/static/plugin/TistoryProfileLayer/style.css" rel="stylesheet" type="text/css"/>
<script type="text/javascript" src="https://tistory1.daumcdn.net/tistory_admin/userblog/userblog-b01726c8aeb47bdb6a378467404d8bd37fde5262/static/plugin/TistoryProfileLayer/script.js"></script>

        <!-- TistoryProfileLayer - END -->

                
                <meta http-equiv="X-UA-Compatible" content="IE=Edge">
<meta name="format-detection" content="telephone=no">
<script src="//t1.daumcdn.net/tistory_admin/lib/jquery/jquery-3.5.1.min.js" integrity="sha256-9/aliU8dGd2tb6OSsuzixeV4y/faTqgFtohetphbbj0=" crossorigin="anonymous"></script>
<script type="text/javascript" src="//t1.daumcdn.net/tiara/js/v1/tiara-1.2.0.min.js"></script><meta name="referrer" content="always"/>
<meta name="google-adsense-platform-account" content="ca-host-pub-9691043933427338"/>
<meta name="google-adsense-platform-domain" content="tistory.com"/>
<meta name="google-adsense-account" content="ca-pub-8136595379682794"/>
<meta name="description" content="linux에서 top 명령어는, linx kernel을 통하여 관리되는 프로세스의 태스크 리스트들의 정보인 CPU, MEM, Process 상태정보등을 확인할 수 있다. top 명령어를 통하여 프로세스가 race condition 상태, 메모리 릭, 과도한 i/o사용률, zombie 프로세스,.. 등 활용하기에 따라 많은 정보를 확인할 수 있다. 그럼 바로 top 명령어를 실행해보자. 화면 설명 상단의 전체 cpu 사용량과 memory사용량, Task 정보와 부팅되고 운영된 up 정보가 나오고 있다. 현재 48 일째 운영되고 있다는 사실을 알 수 있다. CPU 사용율 정보us: CPU time spent in user space user space : i/o wait과 ni를 제외한 processes c.."/>
<meta property="og:type" content="article"/>
<meta property="og:url" content="https://www.morenice.kr/30"/>
<meta property="og.article.author" content="morenice"/>
<meta property="og:site_name" content="morenice's blog"/>
<meta property="og:title" content="top 명령어를 통한 시스템 분석"/>
<meta name="by" content="morenice"/>
<meta property="og:description" content="linux에서 top 명령어는, linx kernel을 통하여 관리되는 프로세스의 태스크 리스트들의 정보인 CPU, MEM, Process 상태정보등을 확인할 수 있다. top 명령어를 통하여 프로세스가 race condition 상태, 메모리 릭, 과도한 i/o사용률, zombie 프로세스,.. 등 활용하기에 따라 많은 정보를 확인할 수 있다. 그럼 바로 top 명령어를 실행해보자. 화면 설명 상단의 전체 cpu 사용량과 memory사용량, Task 정보와 부팅되고 운영된 up 정보가 나오고 있다. 현재 48 일째 운영되고 있다는 사실을 알 수 있다. CPU 사용율 정보us: CPU time spent in user space user space : i/o wait과 ni를 제외한 processes c.."/>
<meta property="og:image" content="https://img1.daumcdn.net/thumb/R800x0/?scode=mtistory2&fname=https%3A%2F%2Ft1.daumcdn.net%2Fcfile%2Ftistory%2F1731AC524E07FB5220"/>
<meta property="article:section" content="'IT 인터넷'"/>
<meta name="twitter:card" content="summary_large_image"/>
<meta name="twitter:site" content="@TISTORY"/>
<meta name="twitter:title" content="top 명령어를 통한 시스템 분석"/>
<meta name="twitter:description" content="linux에서 top 명령어는, linx kernel을 통하여 관리되는 프로세스의 태스크 리스트들의 정보인 CPU, MEM, Process 상태정보등을 확인할 수 있다. top 명령어를 통하여 프로세스가 race condition 상태, 메모리 릭, 과도한 i/o사용률, zombie 프로세스,.. 등 활용하기에 따라 많은 정보를 확인할 수 있다. 그럼 바로 top 명령어를 실행해보자. 화면 설명 상단의 전체 cpu 사용량과 memory사용량, Task 정보와 부팅되고 운영된 up 정보가 나오고 있다. 현재 48 일째 운영되고 있다는 사실을 알 수 있다. CPU 사용율 정보us: CPU time spent in user space user space : i/o wait과 ni를 제외한 processes c.."/>
<meta property="twitter:image" content="https://img1.daumcdn.net/thumb/R800x0/?scode=mtistory2&fname=https%3A%2F%2Ft1.daumcdn.net%2Fcfile%2Ftistory%2F1731AC524E07FB5220"/>
<meta content="https://www.morenice.kr/30" property="dg:plink" content="https://www.morenice.kr/30"/>
<meta name="plink"/>
<meta name="title" content="top 명령어를 통한 시스템 분석"/>
<meta name="article:media_name" content="morenice's blog"/>
<meta property="article:mobile_url" content="https://www.morenice.kr/m/30"/>
<meta property="article:pc_url" content="https://www.morenice.kr/30"/>
<meta property="article:mobile_view_url" content="https://morenice.tistory.com/m/30"/>
<meta property="article:pc_view_url" content="https://morenice.tistory.com/30"/>
<meta property="article:talk_channel_view_url" content="https://www.morenice.kr/m/30"/>
<meta property="article:pc_service_home" content="https://www.tistory.com"/>
<meta property="article:mobile_service_home" content="https://www.tistory.com/m"/>
<meta property="article:txid" content="296044_30"/>
<meta property="article:published_time" content="2011-06-27T13:04:10+09:00"/>
<meta property="og:regDate" content="20110627010410"/>
<meta property="article:modified_time" content="2018-06-14T01:04:28+09:00"/>
<script type="module" src="https://tistory1.daumcdn.net/tistory_admin/userblog/userblog-b01726c8aeb47bdb6a378467404d8bd37fde5262/static/pc/dist/index.js" defer=""></script>
<script type="text/javascript" src="https://tistory1.daumcdn.net/tistory_admin/userblog/userblog-b01726c8aeb47bdb6a378467404d8bd37fde5262/static/pc/dist/index-legacy.js" defer="" nomodule="true"></script>
<script type="text/javascript" src="https://tistory1.daumcdn.net/tistory_admin/userblog/userblog-b01726c8aeb47bdb6a378467404d8bd37fde5262/static/pc/dist/polyfills-legacy.js" defer="" nomodule="true"></script>
<link rel="stylesheet" type="text/css" href="https://t1.daumcdn.net/tistory_admin/www/style/font.css"/>
<link rel="stylesheet" type="text/css" href="https://tistory1.daumcdn.net/tistory_admin/userblog/userblog-b01726c8aeb47bdb6a378467404d8bd37fde5262/static/style/content.css"/>
<link rel="stylesheet" type="text/css" href="https://tistory1.daumcdn.net/tistory_admin/userblog/userblog-b01726c8aeb47bdb6a378467404d8bd37fde5262/static/pc/dist/index.css"/>
<script type="text/javascript">(function() {
    var tjQuery = jQuery.noConflict(true);
    window.tjQuery = tjQuery;
    window.orgjQuery = window.jQuery; window.jQuery = tjQuery;
    window.jQuery = window.orgjQuery; delete window.orgjQuery;
})()</script>
<script type="text/javascript" src="https://tistory1.daumcdn.net/tistory_admin/userblog/userblog-b01726c8aeb47bdb6a378467404d8bd37fde5262/static/script/base.js"></script>
<script type="text/javascript" src="//developers.kakao.com/sdk/js/kakao.min.js"></script>

                
    <title>top 명령어를 통한 시스템 분석 :: morenice's blog</title>
    <meta name="title" content="top 명령어를 통한 시스템 분석 :: morenice's blog" />
    <meta name="description" Content="Information about software engineering" />
    <meta charset="utf-8" />
    <meta name="viewport" content="width=device-width, height=device-height, initial-scale=1, minimum-scale=1.0, maximum-scale=1.0" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge, chrome=1" />
  	<meta name="naver-site-verification" content="710ac14cd77e014481a9491400fe2b2674d418d8" />

    <link rel="alternate" type="application/rss+xml" title="morenice's blog" href="https://morenice.tistory.com/rss" />
    <link rel="shortcut icon" href="https://www.morenice.kr/favicon.ico" />

    <link rel="stylesheet" href="https://tistory1.daumcdn.net/tistory/296044/skin/style.css?_version_=1658112634" />
    <link rel="stylesheet" href="https://tistory1.daumcdn.net/tistory/296044/skin/images/style_webicon.css?_version_=1658112634" />

    <script src="https://cdnjs.cloudflare.com/ajax/libs/jquery/3.3.1/jquery.js"></script>
    <script src="https://tistory1.daumcdn.net/tistory/296044/skin/images/common.js?_version_=1658112634"></script>
	
    <!-- tocbot -->
    <script src="https://cdnjs.cloudflare.com/ajax/libs/tocbot/4.4.2/tocbot.min.js"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/tocbot/4.4.2/tocbot.css">

                
                
                <link rel="stylesheet" type="text/css" href="https://tistory1.daumcdn.net/tistory_admin/userblog/userblog-b01726c8aeb47bdb6a378467404d8bd37fde5262/static/style/revenue.css"/>
<link rel="canonical" href="https://www.morenice.kr/30"/>

<!-- BEGIN STRUCTURED_DATA -->
<script type="application/ld+json">
    {"@context":"http://schema.org","@type":"BlogPosting","mainEntityOfPage":{"@id":"https://www.morenice.kr/30","name":null},"url":"https://www.morenice.kr/30","headline":"top 명령어를 통한 시스템 분석","description":"linux에서 top 명령어는, linx kernel을 통하여 관리되는 프로세스의 태스크 리스트들의 정보인 CPU, MEM, Process 상태정보등을 확인할 수 있다. top 명령어를 통하여 프로세스가 race condition 상태, 메모리 릭, 과도한 i/o사용률, zombie 프로세스,.. 등 활용하기에 따라 많은 정보를 확인할 수 있다. 그럼 바로 top 명령어를 실행해보자. 화면 설명 상단의 전체 cpu 사용량과 memory사용량, Task 정보와 부팅되고 운영된 up 정보가 나오고 있다. 현재 48 일째 운영되고 있다는 사실을 알 수 있다. CPU 사용율 정보us: CPU time spent in user space user space : i/o wait과 ni를 제외한 processes c..","author":{"@type":"Person","name":"morenice","logo":null},"image":{"@type":"ImageObject","url":"https://img1.daumcdn.net/thumb/R800x0/?scode=mtistory2&fname=https%3A%2F%2Ft1.daumcdn.net%2Fcfile%2Ftistory%2F1731AC524E07FB5220","width":"800px","height":"800px"},"datePublished":"2011-06-27T13:04:10+09:00","dateModified":"2018-06-14T01:04:28+09:00","publisher":{"@type":"Organization","name":"TISTORY","logo":{"@type":"ImageObject","url":"https://t1.daumcdn.net/tistory_admin/static/images/openGraph/opengraph.png","width":"800px","height":"800px"}}}
</script>
<!-- END STRUCTURED_DATA -->
<link rel="stylesheet" type="text/css" href="https://tistory1.daumcdn.net/tistory_admin/userblog/userblog-b01726c8aeb47bdb6a378467404d8bd37fde5262/static/style/dialog.css"/>
<link rel="stylesheet" type="text/css" href="//t1.daumcdn.net/tistory_admin/www/style/top/font.css"/>
<link rel="stylesheet" type="text/css" href="https://tistory1.daumcdn.net/tistory_admin/userblog/userblog-b01726c8aeb47bdb6a378467404d8bd37fde5262/static/style/postBtn.css"/>
<link rel="stylesheet" type="text/css" href="https://tistory1.daumcdn.net/tistory_admin/userblog/userblog-b01726c8aeb47bdb6a378467404d8bd37fde5262/static/style/tistory.css"/>
<script type="text/javascript" src="https://tistory1.daumcdn.net/tistory_admin/userblog/userblog-b01726c8aeb47bdb6a378467404d8bd37fde5262/static/script/common.js"></script>

                
                </head>

                                                <body id="tt-body-page" class="thema_black">
                
                
                
    
        <!-- warp / 테마 변경시 thema_xxx 변경 -->
        <div id="wrap" class="thema_black">

            <!-- area_menu -->
            <div class="area_menu">

                <nav class="menu_navigation">																										  
                  <ul class="tt_category"><li class=""><a href="/category" class="link_tit"> 분류 전체보기 </a>
  <ul class="category_list"><li class=""><a href="/category/Introduction" class="link_item"> Introduction </a></li>
<li class=""><a href="/category/Daily" class="link_item"> Daily </a></li>
<li class=""><a href="/category/Review" class="link_item"> Review </a></li>
<li class=""><a href="/category/Think" class="link_item"> Think </a></li>
<li class=""><a href="/category/IT" class="link_item"> IT </a>
  <ul class="sub_category_list"><li class=""><a href="/category/IT/News" class="link_sub_item"> News </a></li>
<li class=""><a href="/category/IT/101" class="link_sub_item"> 101 </a></li>
<li class=""><a href="/category/IT/System%20Design" class="link_sub_item"> System Design </a></li>
<li class=""><a href="/category/IT/Database" class="link_sub_item"> Database </a></li>
<li class=""><a href="/category/IT/Java%20Stack" class="link_sub_item"> Java Stack </a></li>
<li class=""><a href="/category/IT/Python%20Stack" class="link_sub_item"> Python Stack </a></li>
<li class=""><a href="/category/IT/Go%20Stack" class="link_sub_item"> Go Stack </a></li>
<li class=""><a href="/category/IT/Linux%20Kernel" class="link_sub_item"> Linux Kernel </a></li>
<li class=""><a href="/category/IT/Linux%20C" class="link_sub_item"> Linux C </a></li>
<li class=""><a href="/category/IT/DevOps" class="link_sub_item"> DevOps </a></li>
<li class=""><a href="/category/IT/Agile" class="link_sub_item"> Agile </a></li>
<li class=""><a href="/category/IT/Tools" class="link_sub_item"> Tools </a></li>
</ul>
</li>
<li class=""><a href="/category/Blog%20Tips" class="link_item"> Blog Tips </a></li>
</ul>
</li>
</ul>

									<!--  -->
                </nav>

                <div class="m_sidebar pc_blind">
                    <div class="related_posts_mobile">
                        <!-- related_type_view -->
                        <div class="related_type related_type_view" style="display:block;">
                            <ul class="list_related"></ul>
                        </div>
                    </div>
                    <!-- // related_type_view -->

                    <!-- about_me -->
                    <div class="about_me_mobile">
                        <div class="box_sidebar about_me">
                            <h3 class="title_sidebar">ABOUT ME</h3>
                            <p class="text_about">-</p>
                        </div>
                    </div>
                </div>

                <ul class="list_sns">
                    
                    
                        <li><a href="#" class="link_sns link_twitter" target="_blank"><span class="blind">트위터</span></a></li>
                    
                    
                        <li><a href="#" class="link_sns link_insta" target="_blank"><span class="blind">인스타그램</span></a></li>
                    
                </ul>

                <div class="box_visit">
                    <dl class="data_today">
                        <dt class="title_visit">Today</dt>
                        <dd class="item_visit">-</dd>
                    </dl>
                    <dl class="data_yesterday">
                        <dt class="title_visit">Yesterday</dt>
                        <dd class="item_visit">-</dd>
                    </dl>
                    <dl class="data_total">
                        <dt class="title_visit">Total</dt>
                        <dd class="item_visit">-</dd>
                    </dl>
                </div>
            </div>
            <!-- // area_menu -->

            <!-- container  / header에 btn_search 클릭하면 class에 search_on 추가(모바일에서만 작동) -->
            <div id="container">
                <header id="header">
                    <div class="inner_header">
                        <h1 class="logo">
                            <a href="https://www.morenice.kr/" title="morenice's blog" class="link_logo" style="background-image:url('https://tistory1.daumcdn.net/tistory/296044/skinSetting/e43eaed65dd04ed389d6b595f80c184f')">
                                <span class="blind">morenice's blog</span>
                                
                            </a>
                        </h1>
                        <button type="button" class="btn_menu"><span class="icon-Menu"></span><span class="icon-Close"></span><span class="blind">메뉴</span></button>
                        <button class="btn_search"><span class="icon-Search"></span><span class="blind">검색</span></button>

                        <!-- btn_search 클릭하면 나옴 /-->
                        <div class="area_search thema_apply" style="display: none;">
                            <form action="" method="get">
                                <legend><span class="blind">컨텐츠 검색</span></legend>
                                
                                    <input type="text" name="search" title="Search" placeholder="Search"
                                        value="" class="inp_search" onkeypress="if (event.keyCode == 13) { try {
    window.location.href = '/search' + '/' + looseURIEncode(document.getElementsByName('search')[0].value);
    document.getElementsByName('search')[0].value = '';
    return false;
} catch (e) {} }">
                                
                                <button type="button" title="검색어 삭제" class="btn_search_del"></button>
                            </form>
                        </div>

                    </div>
                </header>

                <main id="main">
                    
                    <!-- inner_index -->
                    <div class="inner_index">
                        

                        

                        <!-- category_list -->

                        <div class="category_list index_type_common index_type_horizontal">
                            <ul class="list_horizontal">
                                
    
                    

                    
				<div class='toc'></div>
                        <li class="category_content_area">
                            <!-- area_view_content -->
                            <div class="area_view_content">

                                <!-- article_content -->
                                <div class="article_content">
                                    <div class="info_post">
												<div class="artcle_category_info thema_apply">
													 <a href="/category/IT/DevOps" class="link_category link_slink"><span class="category">IT/DevOps</span></a>
											  </div>
                                        <a href="/30" class="link_title"><div class="title_view">top 명령어를 통한 시스템 분석</div></a>
                                        <div class="view_info_post">
                                            <span class="date">2011. 6. 27.</span>  <span class="comments"><span id="commentCount30_0">6</span> comments</span>
                                        </div>

                                        
                                    </div>

                                    <!-- 본문 내용 영역 -->
                                    <div class="article_view">
                                        <!-- inventory -->
<div data-tistory-react-app="NaverAd"></div>

                    <!-- System - START -->
        <div class="revenue_unit_wrap">
  <div class="revenue_unit_item adsense responsive">
    <div class="revenue_unit_info">반응형</div>
    <script src="//pagead2.googlesyndication.com/pagead/js/adsbygoogle.js" async="async"></script>
    <ins class="adsbygoogle" style="display: block;" data-ad-host="ca-host-pub-9691043933427338" data-ad-client="ca-pub-8136595379682794" data-ad-format="auto"></ins>
    <script>(adsbygoogle = window.adsbygoogle || []).push({});</script>
  </div>
</div>
        <!-- System - END -->

            <div class="contents_style"><p><strong>linux에서 top 명령어는, 
</strong>linx kernel을 통하여 관리되는 프로세스의 태스크 리스트들의 정보인 CPU, MEM, Process 상태정보등을&nbsp;확인할 수 있다.</p>
<p><strong><u>top 명령어를 통하여 프로세스가 race condition 상태, 메모리 릭, 과도한 i/o사용률, zombie 프로세스,.. 등 활용하기에 따라 많은 정보를 확인할 수 있다.</u></strong></p>
<br />
<p>그럼 바로 top 명령어를 실행해보자.</p>

<p style="text-align: center;"><span class="imageblock" style="display: inline-block; width: 750px;  height: auto; max-width: 100%;"><img src="https://t1.daumcdn.net/cfile/tistory/1731AC524E07FB5824" style="max-width: 100%; height: auto;" srcset="https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Ft1.daumcdn.net%2Fcfile%2Ftistory%2F1731AC524E07FB5824" width="750" height="583" filename="실행화면.png" filemime="image/jpeg"/></span></p>

<strong><span style="FONT-SIZE: 14pt">화면 설명</span><br />
</strong>상단의 전체 cpu 사용량과 memory사용량, Task 정보와&nbsp;부팅되고 운영된 up 정보가 나오고 있다.&nbsp;현재 48 일째 운영되고 있다는 사실을 알 수 있다.<br />
<br />
CPU 사용율 정보</p><ul style="list-style-type: disc;"><li><p style="margin-top: 0px; margin-right: 0px; margin-bottom: 0px;">us: CPU time spent in <b>user</b> space&nbsp;</p></li><ul style="list-style-type: disc;"><li><p style="margin-top: 0px; margin-right: 0px; margin-bottom: 0px;">user space : i/o wait과 ni를 제외한&nbsp;processes cpu usage</p></li><li><p style="margin-top: 0px; margin-right: 0px; margin-bottom: 0px;">결국 process들이&nbsp;runing 상태일 때&nbsp;사용율을 의미.</p></li></ul><li><p style="margin-top: 0px; margin-right: 0px; margin-bottom: 0px;"><span style="font-size: 9pt; line-height: 1.5;">sy: CPU time spent in kernel space(<b>system</b>)</span></p></li><ul style="list-style-type: disc;"><li><p style="margin-top: 0px; margin-right: 0px; margin-bottom: 0px;">hardware &amp; software irq &amp; steal time을&nbsp;제외한 kernel cpu usage</p></li><li><p style="margin-top: 0px; margin-right: 0px; margin-bottom: 0px;">가상화 운영이 아닌 경우에는 interrupt를 제외한 kernel cpu 사용율이라고 판단해도 된다.</p></li></ul><li><p style="margin-top: 0px; margin-right: 0px; margin-bottom: 0px;"><span style="font-size: 9pt; line-height: 1.5;">ni: CPU time spent on low priority(<b>nice</b>) processes</span></p></li><ul style="list-style-type: disc;"><li><p style="margin-top: 0px; margin-right: 0px; margin-bottom: 0px;">얼만큼 다른 process들에게 cpu 사용율 친절하게 양보할 것인가를 의미.</p></li><li><p style="margin-top: 0px; margin-right: 0px; margin-bottom: 0px;">의미를 알고 보면&nbsp;<span style="font-size: 9pt; line-height: 1.5;">작명에 높은 점수을 줄 수 있다.</span></p></li><li><p style="margin-top: 0px; margin-right: 0px; margin-bottom: 0px;"><span style="font-size: 9pt; line-height: 1.5;">숫자가 작을수록(특히 음수) higher prioirty를 갖는다.&nbsp;</span></p></li></ul><li><p style="margin-top: 0px; margin-right: 0px; margin-bottom: 0px;"><span style="font-size: 9pt; line-height: 1.5;">id: CPU time spent <b>idle</b></span></p></li><li><p style="margin-top: 0px; margin-right: 0px; margin-bottom: 0px;"><span style="font-size: 9pt; line-height: 1.5;">wa: <b>i/o(disk) wait</b>&nbsp;cpu time&nbsp;</span></p></li><li><p style="margin-top: 0px; margin-right: 0px; margin-bottom: 0px;"><span style="font-size: 9pt; line-height: 1.5;">hi: CPU time spent servicing/handling <b>hardware interrupts</b></span></p></li><li><p style="margin-top: 0px; margin-right: 0px; margin-bottom: 0px;"><span style="font-size: 9pt; line-height: 1.5;">si: CPU time spent servicing/handling <b>software interrupts</b></span></p></li><li><p style="margin-top: 0px; margin-right: 0px; margin-bottom: 0px;"><span style="font-size: 9pt; line-height: 1.5;">st: <b>steal time,&nbsp;</b></span><span style="font-size: 9pt; line-height: 1.5;">CPU time in involuntary wait by virtual cpu while <u>hypervisor</u> is servicing another processor</span></p></li></ul><p style="MARGIN: 0px"><br /></p>
<p></p>
<p style="margin-top: 0px; margin-right: 0px; margin-bottom: 0px;"><strong>만약 us가 아닌&nbsp;인터럽트(hi, si) 혹은 I/O Wait(wa)의 수치가 크게&nbsp;되면 cpu가 다른 작업을 처리하느라 </strong><strong style="font-size: 9pt; line-height: 1.5;">process가 cpu 스케쥴링 당하지 않을 가능성이 높아지기 때문에&nbsp;<u>프로세스 실행 결과 속도가 &nbsp;현저히 떨어질 수 있다.</u></strong></p>
<p style="margin-top: 0px; margin-right: 0px; margin-bottom: 0px;"><span style="font-size: 9pt; line-height: 1.5;"><br /></span></p>
<p style="margin-top: 0px; margin-right: 0px; margin-bottom: 0px;"><span style="font-size: 9pt; line-height: 1.5;">하단에는 Task단위, 즉 프로세스 하나하나의 정보가 나온다.</span></p>
<p></p>
<p></p>
<p style="margin-top: 0px; margin-right: 0px; margin-bottom: 0px;">
<br />
</p>
<p></p>
<p style="text-align: center;"><span class="imageblock" style="display: inline-block; width: 750px;  height: auto; max-width: 100%;"><img src="https://t1.daumcdn.net/cfile/tistory/1531AC524E07FB5723" style="max-width: 100%; height: auto;" srcset="https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Ft1.daumcdn.net%2Fcfile%2Ftistory%2F1531AC524E07FB5723" width="750" height="583" filename="실행화면-설명.png" filemime="image/jpeg"/></span></p>
<p><br />
<br />
<br />
<span style="FONT-SIZE: 14pt"><strong>HELP</strong></span><br />
h(help) 버튼을 누르면 헬프 페이지가 나타난다.<br />
모니터링이 주 목적이기 때문에 화면 배색이나 어떤 정보 위주로 리스트를 sort하여 볼지&nbsp;설정을 할 수 있다.<br />
<br />
<br />
</p>
<p style="text-align: center;"><span class="imageblock" style="display: inline-block; width: 750px;  height: auto; max-width: 100%;"><img src="https://t1.daumcdn.net/cfile/tistory/1931AC524E07FB5321" style="max-width: 100%; height: auto;" srcset="https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Ft1.daumcdn.net%2Fcfile%2Ftistory%2F1931AC524E07FB5321" width="750" height="578" filename="help.png" filemime="image/jpeg"/></span></p>
<p><br />
<br />
<br />
<span style="FONT-SIZE: 14pt"><strong>Sort field</strong></span><br />
<br />
<strong><font color="#e31600">Shift + f&nbsp; (F)</font></strong> &nbsp;키를 눌르면 sort할 컬럼을 선택할 수 있는데,&nbsp;어떤 프로세스가 CPU나 MEM을 &nbsp;많이 쓰고 있는지 확인할 때 유용하게 사용할 수 있다.<br />
<br />
아래는 Shift + f 키를 눌러 나온 화면이다.&nbsp;sort할 필드를 확인후 알파벳을 누르면 *표가 그쪽으로 이동을 합니다.<br />
엔터를 누르면 sort된 화면이 나타난다.<br />
※ 보통 내림차순으로 나오는데,&nbsp;Shift + r (R) 을 누르면 오름차순/내림차순을 변경하여 확인이 가능하다.<br />
<br />
<br />
아래는 Shift + f 을 누른 화면이다.</p>
<p style="text-align: center;"><span class="imageblock" style="display: inline-block; width: 750px;  height: auto; max-width: 100%;"><img src="https://t1.daumcdn.net/cfile/tistory/1231AC524E07FB5522" style="max-width: 100%; height: auto;" srcset="https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Ft1.daumcdn.net%2Fcfile%2Ftistory%2F1231AC524E07FB5522" width="750" height="600" filename="쉬프트 F.png" filemime="image/jpeg"/></span></p>
<p></p>
<p style="MARGIN: 0px"><br />
<strong>Cpu나 Mem 컬럼을 </strong>선택해서 어떤 프로세스가 <u>race condition상태 또는 메모리릭등을&nbsp;확인</u> 할 수 있으며,&nbsp;<strong>Process Status</strong>로 <u>Zombie가 된 프로세스들을 확인 </u>할 수 있다. 태스크 리스트 정보에서 S 컬럼부분에 &nbsp;Z(zombie)라고 나온다.<br />
<br />
<br />
<br />
<strong><span style="FONT-SIZE: 14pt">화면 갱신 주기 설정</span><br />
</strong><br />
아래 화면은 시간 타이머에 의해 갱신이 되는데,<br />
<font color="#e31600"><strong>d(delay)</strong></font>를 누르면 delay 시간, 즉 갱신 주기를 설정할 수 있다.&nbsp; (default 갱신 주기는 3초)<br />
<br />보통&nbsp;1초나 0.5초 주기로 확인을 하는 편이다.<br />
</p>
<p style="text-align: center;"><span class="imageblock" style="display: inline-block; width: 750px;  height: auto; max-width: 100%;"><img src="https://t1.daumcdn.net/cfile/tistory/1731AC524E07FB5220" style="max-width: 100%; height: auto;" srcset="https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Ft1.daumcdn.net%2Fcfile%2Ftistory%2F1731AC524E07FB5220" width="750" height="522" filename="delay설정.png" filemime="image/jpeg"/></span></p>
<p></p>
<p style="TEXT-ALIGN: center; MARGIN: 0px"><strong></strong>&nbsp;</p>
<p style="margin-top: 0px; margin-right: 0px; margin-bottom: 0px;"><br /></p>
<p style="margin-top: 0px; margin-right: 0px; margin-bottom: 0px;"><br /></p>
<p style="margin-top: 0px; margin-right: 0px; margin-bottom: 0px;"><strong><span style="font-size: 14pt;">CPU core별&nbsp;사용율</span></strong></p>
<p style="margin-top: 0px; margin-right: 0px; margin-bottom: 0px;"><br />또한 top의 장점으로&nbsp;Cpu core별 사용율을 볼 수 있다. top 명령 실행 후 <b><u>숫자 "1"을 눌르면 된다.&nbsp;</u></b></p>
<p style="margin-top: 0px; margin-right: 0px; margin-bottom: 0px;">바로 core별 사용율을 확인할 수 있다. 매우 간단하다.&nbsp;<span style="font-size: 9pt; line-height: 1.5;">하지만 이런 결과물들을 실시간 interaction 할 때에만 확인할 수 있는 단점이 있다.</span></p>
<p style="margin-top: 0px; margin-right: 0px; margin-bottom: 0px;">만약 CPU 사용율을 장시간(1일 이상) 모니터링 및 로깅을 하려면 <b>mpstat</b> 도구를 사용하는게 좋다.</p>
<p style="margin-top: 0px; margin-right: 0px; margin-bottom: 0px;"><br /></p>
<p style="margin-top: 0px; margin-right: 0px; margin-bottom: 0px;"><br /></p>
<p style="MARGIN: 0px"><br /></p></div>
                    <!-- System - START -->
        <div class="revenue_unit_wrap">
  <div class="revenue_unit_item adsense responsive">
    <div class="revenue_unit_info">반응형</div>
    <script src="//pagead2.googlesyndication.com/pagead/js/adsbygoogle.js" async="async"></script>
    <ins class="adsbygoogle" style="display: block;" data-ad-host="ca-host-pub-9691043933427338" data-ad-client="ca-pub-8136595379682794" data-ad-format="auto"></ins>
    <script>(adsbygoogle = window.adsbygoogle || []).push({});</script>
  </div>
</div>
        <!-- System - END -->


<div class="container_postbtn #post_button_group">
  <div class="postbtn_like"><script>window.ReactionButtonType = 'reaction';
window.ReactionApiUrl = '//www.morenice.kr/reaction';
window.ReactionReqBody = {
    entryId: 30
}</script>
<div class="wrap_btn" id="reaction-30" data-tistory-react-app="Reaction"></div><div class="wrap_btn wrap_btn_share"><button type="button" class="btn_post sns_btn btn_share" aria-expanded="false" data-thumbnail-url="https://img1.daumcdn.net/thumb/R800x0/?scode=mtistory2&amp;fname=https%3A%2F%2Ft1.daumcdn.net%2Fcfile%2Ftistory%2F1731AC524E07FB5220" data-title="top 명령어를 통한 시스템 분석" data-description="linux에서 top 명령어는, linx kernel을 통하여 관리되는 프로세스의 태스크 리스트들의 정보인 CPU, MEM, Process 상태정보등을 확인할 수 있다. top 명령어를 통하여 프로세스가 race condition 상태, 메모리 릭, 과도한 i/o사용률, zombie 프로세스,.. 등 활용하기에 따라 많은 정보를 확인할 수 있다. 그럼 바로 top 명령어를 실행해보자. 화면 설명 상단의 전체 cpu 사용량과 memory사용량, Task 정보와 부팅되고 운영된 up 정보가 나오고 있다. 현재 48 일째 운영되고 있다는 사실을 알 수 있다. CPU 사용율 정보us: CPU time spent in user space user space : i/o wait과 ni를 제외한 processes c.." data-profile-image="https://tistory1.daumcdn.net/tistory/296044/attach/375516dba18a4462963a701d8cf61e2f" data-profile-name="morenice" data-pc-url="https://www.morenice.kr/30" data-relative-pc-url="/30" data-blog-title="morenice's blog"><span class="ico_postbtn ico_share">공유하기</span></button>
  <div class="layer_post" id="tistorySnsLayer"></div>
</div><div class="wrap_btn wrap_btn_etc" data-entry-id="30" data-entry-visibility="public" data-category-visibility="public"><button type="button" class="btn_post btn_etc2" aria-expanded="false"><span class="ico_postbtn ico_etc">게시글 관리</span></button>
  <div class="layer_post" id="tistoryEtcLayer"></div>
</div></div>
<button type="button" class="btn_menu_toolbar btn_subscription #subscribe" data-blog-id="296044" data-url="https://www.morenice.kr/30" data-device="web_pc" data-tiara-action-name="구독 버튼_클릭"><em class="txt_state"></em><strong class="txt_tool_id">morenice's blog</strong><span class="img_common_tistory ico_check_type1"></span></button><div class="postbtn_ccl" data-ccl-type="1" data-ccl-derive="2">
    <a href="https://creativecommons.org/licenses/by-nc-nd/4.0/deed.ko" target="_blank" class="link_ccl" rel="license">
        <span class="bundle_ccl">
            <span class="ico_postbtn ico_ccl1">저작자표시</span> <span class="ico_postbtn ico_ccl2">비영리</span> <span class="ico_postbtn ico_ccl3">변경금지</span> 
        </span>
        <span class="screen_out">(새창열림)</span>
    </a>
</div>
<!--
<rdf:RDF xmlns="https://web.resource.org/cc/" xmlns:dc="https://purl.org/dc/elements/1.1/" xmlns:rdf="https://www.w3.org/1999/02/22-rdf-syntax-ns#">
    <Work rdf:about="">
        <license rdf:resource="https://creativecommons.org/licenses/by-nc-nd/4.0/deed.ko" />
    </Work>
    <License rdf:about="https://creativecommons.org/licenses/by-nc-nd/4.0/deed.ko">
        <permits rdf:resource="https://web.resource.org/cc/Reproduction"/>
        <permits rdf:resource="https://web.resource.org/cc/Distribution"/>
        <requires rdf:resource="https://web.resource.org/cc/Notice"/>
        <requires rdf:resource="https://web.resource.org/cc/Attribution"/>
        <prohibits rdf:resource="https://web.resource.org/cc/CommercialUse"/>

    </License>
</rdf:RDF>
-->  <div data-tistory-react-app="SupportButton"></div>
</div>

                                    </div>

                                    
                                        <!-- area_tag -->
                                        <div class="area_tag">
                                            <h2 class="title_tag">TAG</h2>
                                            <div class="tag_content"><a href="/tag/linux" rel="tag">linux</a>, <a href="/tag/program" rel="tag">program</a>, <a href="/tag/Top" rel="tag">Top</a>, <a href="/tag/%EC%8B%9C%EC%8A%A4%ED%85%9C%EB%B6%84%EC%84%9D" rel="tag">시스템분석</a></div>
                                        </div>
                                        <!-- // area_tag -->
                                    


                                    
                                        <!-- related_type_view -->
                                        <div class="related_type related_type_view">
                                            <h2 class="title_related">관련글 <a href="/category/IT/DevOps"
                                                    class="link_add thema_apply">관련글 더보기</a></h2>
                                            <ul class="list_related">
                                                
                                                    <li>
                                                        <a href="/34?category=515509"
                                                            class="link_related" >
                                                            <span class="bg"></span>
                                                            <span class="txt"><strong>ldd 라이브러리 참조 확인 도구</strong></span>
                                                        </a>
                                                    </li>
                                                
                                                    <li>
                                                        <a href="/31?category=515509"
                                                            class="link_related" >
                                                            <span class="bg"></span>
                                                            <span class="txt"><strong>linux 디렉토리 구조</strong></span>
                                                        </a>
                                                    </li>
                                                
                                                    <li>
                                                        <a href="/27?category=515509"
                                                            class="link_related" >
                                                            <span class="bg"></span>
                                                            <span class="txt"><strong>ltrace 도구</strong></span>
                                                        </a>
                                                    </li>
                                                
                                                    <li>
                                                        <a href="/23?category=515509"
                                                            class="link_related" >
                                                            <span class="bg"></span>
                                                            <span class="txt"><strong>strace 디버깅 도구</strong></span>
                                                        </a>
                                                    </li>
                                                
                                            </ul>
                                        </div>
                                        <!-- // related_type_view -->
                                    

                                    <!-- area_comment -->
                                    <div class="area_reply">
                                        <div class="box_reply_info">
                                            <a href="#rp" onclick="" class="reply_events">
                                            <p class="item_info">댓글 <span class="thema_apply">
                                                    <span id="commentCount30_1">6</span>
                                                </span></p>
                                            </a>
                                            <button type="button" class="btn_fold"><span class="blind">댓글
                                                    접기</span></button>
                                            <button type="button" class="btn_spread" style="display: none;"><span
                                                    class="blind">댓글 펼치기</span></button>
                                        </div>

                                        <div data-tistory-react-app="Namecard"></div><div id="entry30Comment">
                                            <!-- reply_content -->
                                            <div class="reply_content">
                                                <button type="button" class="btn_more btn_replymore"
                                                    style="display: none;">이전 댓글 더보기</button>

                                                <!-- box_comment_list -->
                                                <div class="box_comment_list">
                                                    
                                                        <div class="comment-list">
                                                            <ul>
                                                                            

            <li id="none_display_division_for_comment_list_30" style="display: none;"></li>
<script type="text/javascript">
    setInitialEntryComments(30, 1764164925)
</script>
                                                            </ul>
                                                        </div>
                                                    
                                                </div>
                                                <!-- // box_comment_list -->

                                                <form method="post" action="/comment/add/30" onsubmit="return false" style="margin: 0">
    
                                        <!-- reply_write -->
                                        <form method="post">
                                            <div class="reply_write">

                                                <div class="form_content thema_apply">
                                                    <textarea id="comment"
                                                        name="comment"
                                                        placeholder="댓글을 입력해주세요."></textarea>
                                                </div>
                                                
                                                    
                                                        <div class="form_guest">
                                                            <div class="box_inp">
                                                                <div class="inner_inp">
                                                                    <input type="text" name="name"
                                                                        value="" title="이름"
                                                                        placeholder="이름"
                                                                        class="inp_comment inp_name" />
                                                                </div>
                                                            </div>
                                                            <div class="box_inp">
                                                                <div class="inner_inp">
                                                                    <input type="password"
                                                                        name="password"
                                                                        value="" title="비밀번호"
                                                                        maxlength="12"
                                                                        placeholder="비밀번호"
                                                                        class="inp_comment inp_password" />
                                                                </div>
                                                            </div>
                                                        </div>
                                                    

                                                    <div class="form_reg">
                                                        <label><input type="checkbox" name="secret">
                                                            비밀글</label>
                                                    </div>
                                                

                                                <div class="form_reg">
                                                    <button type="button" class="btn_register thema_apply"
                                                        onclick="addComment(this, 30); return false;">등록</button>
                                                </div>
                                            </div>
                                        </form>
                                        <!-- // reply_write -->
                                    
</form>

                                            </div>
                                            <!-- // reply_content -->
                                        </div>
<script type="text/javascript">loadedComments[30]=true;
findFragmentAndHighlight(30);</script>

                                    </div>
                                    <!-- // area_comment -->

                                </div>
                                <!-- article_content -->

                            </div>
                        </li>
                    
                
    

                            </ul>
                        </div>

                        

                        

                        

                        

                        

                        

                        


                    </div>
                    <!-- // inner_index -->

                </main>

                <!-- aside -->
                <aside class="sidebar mobile_blind">
                    <div class="inner_sidebar thema_apply">
                                    <div class="revenue_unit_wrap">
  <div class="revenue_unit_item adsense responsive">
    <div class="revenue_unit_info">반응형</div>
    <script src="//pagead2.googlesyndication.com/pagead/js/adsbygoogle.js" async="async"></script>
    <ins class="adsbygoogle" style="display: block;" data-ad-host="ca-host-pub-9691043933427338" data-ad-client="ca-pub-8136595379682794" data-ad-format="auto"></ins>
    <script>(adsbygoogle = window.adsbygoogle || []).push({});</script>
  </div>
</div>
                                <!-- 인기포스트 -->
                                <div class="related_posts">
                                    <div class="related_type related_type_view">
                                        <h2 class="title_related">인기포스트</h2>
                                        <ul class="list_related">
                                            
                                                <li>
                                                    <a href="/256" class="link_related" style="background-image:url('https://img1.daumcdn.net/thumb/R750x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdna%2F51Aur%2FbtqXXjB4QFR%2FAAAAAAAAAAAAAAAAAAAAAIBh_OlqRaDC2X7e9fhGgih1y9Yt1_B1VJf9lFfzNnxb%2Fimg.png%3Fcredential%3DyqXZFxpELC7KVnFOS48ylbz2pIh7yKj8%26expires%3D1764514799%26allow_ip%3D%26allow_referer%3D%26signature%3Dt%252Fk4mmqw2eTBIgE7G%252FQo66V9TsQ%253D')">
                                                        <span class="bg"></span>
                                                        <span class="txt"><strong>맥북 프로 잠자기 배터리 광탈</strong></span>
                                                    </a>
                                                </li>
                                            
                                                <li>
                                                    <a href="/119" class="link_related" >
                                                        <span class="bg"></span>
                                                        <span class="txt"><strong>ubuntu 데스크탑과 서버 커널의 차이점은?</strong></span>
                                                    </a>
                                                </li>
                                            
                                                <li>
                                                    <a href="/272" class="link_related" style="background-image:url('https://img1.daumcdn.net/thumb/R750x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdna%2FLfJOh%2Fbtrx18qZnah%2FAAAAAAAAAAAAAAAAAAAAABOb-ubEbhIH4k8a-11uhaiOts7R09GEmJrqogdFRjID%2Fimg.png%3Fcredential%3DyqXZFxpELC7KVnFOS48ylbz2pIh7yKj8%26expires%3D1764514799%26allow_ip%3D%26allow_referer%3D%26signature%3DOHONWQ%252BBQFXuZgQTeZDXVdeOc%252Fo%253D')">
                                                        <span class="bg"></span>
                                                        <span class="txt"><strong>Google One 멤버쉽 구독</strong></span>
                                                    </a>
                                                </li>
                                            
                                                <li>
                                                    <a href="/72" class="link_related" >
                                                        <span class="bg"></span>
                                                        <span class="txt"><strong>프로세스가 열고 있는 파일을 확인하는 방법 - lsof</strong></span>
                                                    </a>
                                                </li>
                                            
                                        </ul>
                                    </div>
                                </div>
                            
                                <!-- 블로그 정보 -->
                                <div class="about_me_pc">
                                    <div class="box_sidebar about_me">
                                        <div class="inbox">
                                            <h3 class="title_sidebar">ABOUT ME</h3>
                                            <p class="text_about">Information about software engineering</p>
                                        </div>
                                    </div>
                                </div>
                            
                                <!-- 링크 -->
                                <div class="box_sidebar">
                                    <div class="inbox">
                                        <h3 class="title_sidebar">LINK</h3>
                                        
                                            <a href="http://www.packetinside.com/" class="link_slink">Packet Inside</a>
                                        
                                            <a href="http://channy.creation.net/" class="link_slink">Channy's Blog</a>
                                        
                                            <a href="http://recipes.egloos.com/" class="link_slink">친절한 임베디드 시스템 개발자 되기 강좌</a>
                                        
                                            <a href="https://zoningout.tistory.com" class="link_slink">일상에서 멍때리기</a>
                                        
                                            <a href="https://software-craftsman.tistory.com" class="link_slink">software-craftsman</a>
                                        
                                            <a href="http://blog.naver.com/marronkoal" class="link_slink">코알</a>
                                        
                                    </div>
                                </div>
                            
                                <!-- 관리자 메뉴 -->
                                <div class="box_sidebar sidebar_admin">
                                    <div class="inbox">
                                        <h3 class="title_sidebar">ADMIN</h3>
                                        <a href="https://morenice.tistory.com/manage" class="admin"><span class="blind">admin</span></a>
                                        <a href="https://morenice.tistory.com/manage/entry/post" class="write"><span class="blind">글쓰기</span></a>
                                    </div>
                                </div>
                            
                                <!-- 방문자수 -->
                                <div class="box_sidebar visit_counter">
                                    <div class="inbox">
                                        <span class="total">994,847</span>
                                        <span class="today">12</span>
                                        <span class="yesterday">12</span>
                                    </div>
                                </div>
                            
                    </div>
                </aside>
                <!-- // aside -->

                <!-- footer -->
                
                <footer id="footer">
                    Designed by Tistory.
                </footer>
                <!-- // footer -->

            </div>
            <!-- // container -->

        </div>
        <!-- // wrap -->
    

<div class="#menubar menu_toolbar toolbar_rb">
  <h2 class="screen_out">티스토리툴바</h2>
<div class="btn_tool"><button class="btn_menu_toolbar btn_subscription  #subscribe" data-blog-id="296044" data-url="https://morenice.tistory.com" data-device="web_pc"><strong class="txt_tool_id">morenice's blog</strong><em class="txt_state">구독하기</em><span class="img_common_tistory ico_check_type1"></span></button></div></div>
<div class="#menubar menu_toolbar "></div>
<div class="layer_tooltip">
  <div class="inner_layer_tooltip">
    <p class="desc_g"></p>
  </div>
</div>
<div id="editEntry" style="position:absolute;width:1px;height:1px;left:-100px;top:-100px"></div>


                        <!-- CallBack - START -->
        <script>                    (function () { 
                        var blogTitle = 'morenice\'s blog';
                        
                        (function () {
    function isShortContents () {
        return window.getSelection().toString().length < 30;
    }
    function isCommentLink (elementID) {
        return elementID === 'commentLinkClipboardInput'
    }

    function copyWithSource (event) {
        if (isShortContents() || isCommentLink(event.target.id)) {
            return;
        }
        var range = window.getSelection().getRangeAt(0);
        var contents = range.cloneContents();
        var temp = document.createElement('div');

        temp.appendChild(contents);

        var url = document.location.href;
        var decodedUrl = decodeURI(url);
        var postfix = ' [' + blogTitle + ':티스토리]';

        event.clipboardData.setData('text/plain', temp.innerText + '\n출처: ' + decodedUrl + postfix);
        event.clipboardData.setData('text/html', '<pre data-ke-type="codeblock">' + temp.innerHTML + '</pre>' + '출처: <a href="' + url + '">' + decodedUrl + '</a>' + postfix);
        event.preventDefault();
    }

    document.addEventListener('copy', copyWithSource);
})()

                    })()</script>

        <!-- CallBack - END -->

<!-- DragSearchHandler - START -->
<script src="//search1.daumcdn.net/search/statics/common/js/g/search_dragselection.min.js"></script>

<!-- DragSearchHandler - END -->

        <!-- NaverAnalytics - START -->
        <script type="text/javascript" src="//wcs.naver.net/wcslog.js"></script>
<script type="text/javascript">if(!wcs_add) var wcs_add = {};
   wcs_add["wa"] = encodeURI("7394bd067e3010");
   wcs_do();</script>

        <!-- NaverAnalytics - END -->

        <!-- SyntaxHighlight - START -->
        <link href="//cdnjs.cloudflare.com/ajax/libs/highlight.js/10.7.3/styles/monokai.min.css" rel="stylesheet"/><script src="//cdnjs.cloudflare.com/ajax/libs/highlight.js/10.7.3/highlight.min.js"></script>
<script src="//cdnjs.cloudflare.com/ajax/libs/highlight.js/10.7.3/languages/delphi.min.js"></script>
<script src="//cdnjs.cloudflare.com/ajax/libs/highlight.js/10.7.3/languages/php.min.js"></script>
<script src="//cdnjs.cloudflare.com/ajax/libs/highlight.js/10.7.3/languages/python.min.js"></script>
<script src="//cdnjs.cloudflare.com/ajax/libs/highlight.js/10.7.3/languages/r.min.js" defer></script>
<script src="//cdnjs.cloudflare.com/ajax/libs/highlight.js/10.7.3/languages/ruby.min.js"></script>
<script src="//cdnjs.cloudflare.com/ajax/libs/highlight.js/10.7.3/languages/scala.min.js" defer></script>
<script src="//cdnjs.cloudflare.com/ajax/libs/highlight.js/10.7.3/languages/shell.min.js"></script>
<script src="//cdnjs.cloudflare.com/ajax/libs/highlight.js/10.7.3/languages/sql.min.js"></script>
<script src="//cdnjs.cloudflare.com/ajax/libs/highlight.js/10.7.3/languages/swift.min.js" defer></script>
<script src="//cdnjs.cloudflare.com/ajax/libs/highlight.js/10.7.3/languages/typescript.min.js" defer></script>
<script src="//cdnjs.cloudflare.com/ajax/libs/highlight.js/10.7.3/languages/vbnet.min.js" defer></script>
  <script>hljs.initHighlightingOnLoad();</script>


        <!-- SyntaxHighlight - END -->

                
                <div style="margin:0; padding:0; border:none; background:none; float:none; clear:none; z-index:0"></div>
<script type="text/javascript" src="https://tistory1.daumcdn.net/tistory_admin/userblog/userblog-b01726c8aeb47bdb6a378467404d8bd37fde5262/static/script/common.js"></script>
<script type="text/javascript">window.roosevelt_params_queue = window.roosevelt_params_queue || [{channel_id: 'dk', channel_label: '{tistory}'}]</script>
<script type="text/javascript" src="//t1.daumcdn.net/midas/rt/dk_bt/roosevelt_dk_bt.js" async="async"></script>

                
                <script>window.tiara = {"svcDomain":"user.tistory.com","section":"글뷰","trackPage":"글뷰_보기","page":"글뷰","key":"296044-30","customProps":{"userId":"0","blogId":"296044","entryId":"30","role":"guest","trackPage":"글뷰_보기","filterTarget":false},"entry":{"entryId":"30","entryTitle":"top 명령어를 통한 시스템 분석","entryType":"POST","categoryName":"IT/DevOps","categoryId":"515509","serviceCategoryName":"IT 인터넷","serviceCategoryId":401,"author":"297860","authorNickname":"morenice","blogNmae":"morenice's blog","image":"cfile7.uf@1731AC524E07FB52200E30.png","plink":"/30","tags":["linux","program","Top","시스템분석"]},"kakaoAppKey":"3e6ddd834b023f24221217e370daed18","appUserId":"null"}</script>
<script type="module" src="https://t1.daumcdn.net/tistory_admin/frontend/tiara/v1.0.5/index.js"></script>
<script src="https://t1.daumcdn.net/tistory_admin/frontend/tiara/v1.0.5/polyfills-legacy.js" nomodule="true" defer="true"></script>
<script src="https://t1.daumcdn.net/tistory_admin/frontend/tiara/v1.0.5/index-legacy.js" nomodule="true" defer="true"></script>

                </body>
<script>
    $('.article_content').find('table').each(function (idx, el) {
        $(el).wrap('<div class="table-overflow">')
    })
</script>

<script>
    // init tocbot(본문 목차 자동생성)
    var content = document.querySelector('.article_view')
    var headings = content.querySelectorAll('h1, h2, h3, h4, h5, h6, h7')
    var headingMap = {}
    Array.prototype.forEach.call(headings, function (heading) {
        var id = heading.id ? heading.id : heading.textContent.trim().toLowerCase()
          .split(' ').join('-').replace(/[\!\@\#\$\%\^\&\*\(\):]/ig, '')
        headingMap[id] = !isNaN(headingMap[id]) ? ++headingMap[id] : 0
        if (headingMap[id]) {
            heading.id = id + '-' + headingMap[id]
          } else {
              heading.id = id
            }
      })
	
    tocbot.init({
        tocSelector: '.toc',
        contentSelector: '.article_view',
        headingSelector:'h1, h2, h3',
        hasInnerContainers: false
      });
	
    $(document).ready(function(){
        $('.toc').addClass('toc-absolute');
			
        // var toc_top = $('.toc').offset().top - 165;
        // $(window).scroll(function() {
        //     if ($(this).scrollTop() >= toc_top) {
        //         $('.toc').addClass('toc-fixed');
        //         $('.toc').removeClass('toc-absolute');
        //       } else {
        //           $('.toc').addClass('toc-absolute');
        //           $('.toc').removeClass('toc-fixed');
        //         }
        //   });
        $('.toc').addClass('toc-fixed');
        $('.toc').removeClass('toc-absolute');
        
      });
</script>

</html>
[오픈소 스과제.htm](https://github.com/user-attachments/files/23772724/default.htm)
)



## top(탑) 사용법

+  top
+  top -o %CPU
+  top -o %MEM


---

# 🧾 ps

**ps** 명령어는 현재 실행 중인 프로세스를 보여줍니다.

## 🔧 사용법
```
1 ps
2 ps aux
3 ps -ef
```

---

# 📂 jobs

**jobs** 명령어는 현재 셸에서 실행 중인 작업 목록을 확인합니다.

## 🔧 사용법
```
jobs
fg %1
bg %1
```

---

# ❌ kill

**kill** 명령어는 프로세스를 종료할 때 사용합니다.

## 🔧 사용법
```
kill <PID>
kill -9 <PID>
kill -15 <PID>
```

---
