
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Play</title>
    <link rel="shortcut icon" type="image/png" href="/img/media/favicon.png" />
    <link rel="stylesheet" href="https://wow.truefriend.life/css/bootstrap.min.css">
    <link rel="stylesheet" href="https://wow.truefriend.life/css/mycss.css">
    <link rel="stylesheet" href="https://wow.truefriend.life/css/my-css4ads.css">
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;500;600;700&display=swap" rel="stylesheet">
    <script defer src="https://kit.fontawesome.com/47eafd82ac.js" crossorigin="anonymous"></script>
</head>
<body>
    <!-- Google Tag Manager -->
    <script async src="https://www.googletagmanager.com/gtm.js?id=GTM-NX3TNSFB"></script>

    <!-- Facebook Pixel -->
    <script>
        !function(f,b,e,v,n,t,s) {
            if(f.fbq)return;n=f.fbq=function(){n.callMethod?
            n.callMethod.apply(n,arguments):n.queue.push(arguments)};
            if(!f._fbq)f._fbq=n;n.push=n;n.loaded=!0;n.version='2.0';
            n.queue=[];t=b.createElement(e);t.async=!0;
            t.src=v;s=b.getElementsByTagName(e)[0];
            s.parentNode.insertBefore(t,s)}(window, document,'script',
            'https://connect.facebook.net/en_US/fbevents.js');
        fbq('init', '382976396637351');
        fbq('track', 'PageView');
    </script>
    <noscript><img height="1" width="1" style="display:none"
        src="https://www.facebook.com/tr?id=382976396637351&ev=PageView&noscript=1"
    /></noscript>

    <!-- OneSignal Push Notifications -->
    <script src="https://cdn.onesignal.com/sdks/OneSignalSDK.js" async></script>
    <script>
        window.OneSignal = window.OneSignal || [];
        OneSignal.push(function() {
            OneSignal.init({
                appId: "11bb9994-cb91-4b14-9c2c-0c74245a4801",
            });
        });
    </script>

    <!-- Custom Scripts -->
    <script>
        function validate() {                
            var audio=document.getElementById("mClick"); // sound play 
            audio.play();
            if ($.trim($("#player_name").val()) != "") {
                var regex = /^[A-Za-z0-9 ]+$/;
                var isValid = regex.test(document.getElementById("player_name").value);
                if (!isValid) {
                    $("#player_name").addClass("alertEmptyText");
                    document.querySelector("p.text-danger").style.display="block";
                    document.querySelector("p.text-danger").innerHTML="Special Characters[@,!.- etc not allowed]";
                    return false;
                } else {
                    return true;
                }
            } else {
                $("#player_name").addClass("alertEmptyText");
                document.querySelector("p.text-danger").style.display="block";
                document.querySelector("p.text-danger").innerHTML="Please Enter Your Name!";
                return false;
            }
        }
    </script>

    <nav class="navbar navbar-dark py-0">
        <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarTogglerDemo02" aria-controls="navbarTogglerDemo02" aria-expanded="false" aria-label="Toggle navigation">
            <span></span><span></span><span></span>
        </button>
        <a class="navbar-brand" href="https://truefriend.life">
            <div class="logoText">Friendship Quiz</div>
        </a>
        <div class="center">
            <div><img src="https://wow.truefriend.life/img/media/lang2.png" /></div>
            <select class="lang" id="Lselect" onchange="changeLang()">
                <option value="en">English</option>
                <option value="fr">Français</option>
            </select>
        </div>
        <div class="collapse navbar-collapse" id="navbarTogglerDemo02">
            <ul class="navbar-nav ml-auto mt-2 mt-lg-0">
                <li class="nav-item"><a class="nav-link" href="https://truefriend.life">Home</a></li>
                <li class="nav-item"><a class="nav-link" href="https://truefriend.life/about-us.html">About Us</a></li>
                <li class="nav-item"><a class="nav-link" href="https://truefriend.life/social.html">Social</a></li>
                <li class="nav-item"><a class="nav-link" href="https://truefriend.life/contact-us.html">Contact Us</a></li>
            </ul>
        </div>
    </nav>

    <div class="my-container">
        <div class="row mx-auto">
            <div class="card" id="firstCard">
                <div class="img_div">
                    <h3 style="color: rgb(21,76,82);text-align:center;margin:20px;background-color: floralwhite;border-radius:10px;">
                         <br/> 
                    </h3>
                    <div class="instructions">
                        <h4 class="heading">Instructions</h4>
                        <ul>
                            <li><span class="red"></span>Enter your name.</li>
                           
                        </ul>
                    </div>
                    <div class="group1" id="input-name">
                        <p class="validation-text"></p>
                        <form method="POST" action="https://wow.truefriend.life/play-now/DOd5WsdQ" onsubmit="return validate()">
                            <fieldset>
                                <div><input type="text" name="name_of_player" id="player_name" value autocomplete="on" placeholder="✍🏻 Enter your name." /></div>
                                <input type="hidden" name="_token" value="7FdyEqqIp8VXkyE4WSFAB6AjBilvtWK6r6AjXNdV" />
                                <p class="text-danger" style="display: none;"></p>
                                <div><input class="button-24" type="submit" id="start" value="Start" /></div>
                            </fieldset>
                        </form>
                        <audio id="mClick" preload="auto">
                            <source src="/pub_resources/mouseclick.mp3" type="audio/mpeg" />Your browser does not support the audio element.
                        </audio>
                    </div>
                </div>
            </div>
        </div>
        <div class="scoreboard" style="display:block">
            <br/>

            <br/><br/>
            
        </div>
        <div id="ezoic-pub-ad-placeholder-145"> </div>
        <div class="cross-site-links">
            <p style="margin-bottom:-5px;">Advertisement</p>
            <a target="_blank" href="https://truefriend.life/index1.html">
                <img src="/img/media/true_friendship_challenge.png" alt="true_friendship_challenge" />
            </a>
        </div>
        <div class="cross-site-links">
           </a>
        </div>
    </div>

 
</body>
</html>
