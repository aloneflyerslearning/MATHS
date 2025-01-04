<!DOCTYPE html>
<html lang="hi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>कक्षा 10 गणित प्रश्नोत्तरी (Class 10 Maths Quiz)</title>
    <style>
        body { font-family: 'Arial', sans-serif; line-height: 1.6; margin: 20px; color:#333;}
        h1, h2 { text-align: center; margin-bottom: 20px; }
        .quiz-container { margin: 20px auto; max-width: 700px; padding: 20px; border: 1px solid #ddd; border-radius: 8px; background-color: #f9f9f9; }
        .question { margin-bottom: 15px; border-bottom: 1px solid #eee; padding-bottom: 10px; }
         .tabs { display: flex; justify-content: center; margin-bottom: 20px; }
        .tab { padding: 10px 20px; background-color: #f0f0f0; border: 1px solid #ccc; border-radius: 4px 4px 0 0; cursor: pointer; margin: 0 5px; }
          .tab.active { background-color: #ddd; border-bottom: 1px solid #ddd; }
         .tab-content { display: none; padding: 10px; }
         .tab-content.active { display: block; }
        .options label { display: block; margin-bottom: 5px; }
        button { display: block; margin-top: 20px; padding: 10px 20px; background-color: #5cb85c; color: white; border: none; border-radius: 4px; cursor: pointer; }
        button:hover { background-color: #4cae4c; }
        #results { margin-top: 30px; padding: 20px; border: 1px solid #ddd; border-radius: 8px; background-color: #fff; text-align: center;}
          #participants{ margin-top: 30px; padding: 20px; border: 1px solid #ddd; border-radius: 8px; background-color: #fff; text-align: center;}
        #participants ul{ list-style: none; padding:0; margin:0;}
        #participants li { margin-bottom: 5px; }
        .correct { color: green; }
        .incorrect { color: red; }
    </style>
</head>
<body>
    <header>
        <h1>कक्षा 10 गणित प्रश्नोत्तरी</h1>
    </header>
    <main>
       <div class="tabs">
            <div class="tab active" data-tab="quiz1">क्विज़ 1</div>
             <div class="tab" data-tab="quiz2">क्विज़ 2</div>
              <div class="tab" data-tab="quiz3">क्विज़ 3</div>
                <div class="tab" data-tab="quiz4">क्विज़ 4</div>
        </div>

        <div class="quiz-container">
            <form id="quiz1" class="tab-content active" >
            </form>
            <form id="quiz2" class="tab-content" >
            </form>
            <form id="quiz3" class="tab-content" >
            </form>
            <form id="quiz4" class="tab-content" >
            </form>
       </div>


        <div id="results" style="display: none;"></div>
          <div id="participants" style="display: none;"></div>
    </main>

    <script>
        const questions = {
             quiz1: [
                {
                     question: "10 और 20 का महत्तम समापवर्तक (HCF) क्या है?",
                     options: ["2", "5", "10", "20"],
                     correctAnswer: "10"
                },
                {
                     question: "एक द्विघात समीकरण का रूप क्या है?",
                    options: ["ax+b=0", "ax^2+bx+c=0", "ax^3+bx^2+c=0", "ax+b+c=0"],
                     correctAnswer: "ax^2+bx+c=0"
                 },
                 {
                    question: "त्रिभुज के तीन कोणों का योग कितना होता है?",
                    options: ["90", "180", "270", "360"],
                    correctAnswer: "180"
                },
                   {
                    question: "π (पाई) का मान क्या है?",
                     options: ["2.14", "3.14", "4.14", "5.14"],
                    correctAnswer: "3.14"
                 },
                 {
                    question: "एक वृत्त की त्रिज्या 7 सेमी है, तो उसका क्षेत्रफल क्या होगा?",
                   options: ["154 सेमी²", "128 सेमी²", "136 सेमी²", "142 सेमी²"],
                    correctAnswer: "154 सेमी²"
                },
                {
                    question: "रेखा 2x + 3y = 6 का ढाल क्या है?",
                   options: ["-2/3", "2/3", "3/2", "-3/2"],
                   correctAnswer: "-2/3"
                 },
                {
                    question: "यदि एक त्रिभुज की दो भुजाएँ 3 सेमी और 4 सेमी हैं, और दोनों के बीच का कोण 90 डिग्री है, तो तीसरी भुजा की लंबाई क्या होगी?",
                   options: ["5 सेमी", "7 सेमी", "10 सेमी", "12 सेमी"],
                     correctAnswer: "5 सेमी"
                 },
                {
                    question: "शंकु का आयतन का सूत्र क्या है?",
                   options: ["1/3πr^2h", "πr^2h", "2πrh", "4/3πr^3"],
                    correctAnswer: "1/3πr^2h"
                },
                   {
                     question: "1 और 100 के बीच कितने अभाज्य संख्याएं हैं?",
                     options: ["20", "25", "30", "35"],
                     correctAnswer: "25"
                },
                {
                    question: "यदि sinθ = 1/2, तो θ का मान क्या है?",
                     options: ["30 डिग्री", "45 डिग्री", "60 डिग्री", "90 डिग्री"],
                     correctAnswer: "30 डिग्री"
                },
                {
                     question: "एक आयत का क्षेत्रफल का सूत्र क्या है?",
                     options: ["लंबाई + चौड़ाई", "2(लंबाई + चौड़ाई)", "लंबाई × चौड़ाई", "4 × भुजा"],
                     correctAnswer: "लंबाई × चौड़ाई"
                },
                 {
                    question: "एक घन का आयतन का सूत्र क्या है?",
                    options: ["भुजा^2", "भुजा^3", "4 × भुजा", "6 × भुजा^2"],
                    correctAnswer: "भुजा^3"
                 },
                   {
                    question: "एक घनाभ का कुल पृष्ठीय क्षेत्रफल का सूत्र क्या है?",
                    options: ["2(lb + bh + hl)", "lbh", "2πr(r + h)", "4πr^2"],
                    correctAnswer: "2(lb + bh + hl)"
                 },
                {
                     question: "एक बेलन का आयतन का सूत्र क्या है?",
                    options: ["πr^2h", "2πrh", "1/3πr^2h", "4/3πr^3"],
                    correctAnswer: "πr^2h"
                 },
                 {
                    question: "एक गोले का पृष्ठीय क्षेत्रफल का सूत्र क्या है?",
                    options: ["2πr^2", "4πr^2", "πr^2", "2πrh"],
                     correctAnswer: "4πr^2"
                 },
                  {
                    question: "12 और 15 का लघुत्तम समापवर्त्य (LCM) क्या है?",
                    options: ["30", "45", "60", "75"],
                     correctAnswer: "60"
                },
                   {
                     question: "एक वृत्त का परिधि का सूत्र क्या है?",
                    options: ["πr^2", "2πr", "πd", "4πr^2"],
                    correctAnswer: "2πr"
                },
                 {
                    question: "एक वर्ग का क्षेत्रफल का सूत्र क्या है?",
                    options: ["4 × भुजा", "2 × भुजा", "भुजा^2", "भुजा^3"],
                    correctAnswer: "भुजा^2"
                 },
                 {
                    question: "बिंदुओं (x1, y1) और (x2, y2) के बीच की दूरी का सूत्र क्या है?",
                    options: ["√((x2-x1)²+(y2-y1)²) ", "x2-x1+y2-y1", "(x2-x1)²+(y2-y1)²", "√((x2+x1)²+(y2+y1)²)"],
                     correctAnswer: "√((x2-x1)²+(y2-y1)²)"
                 },
                 {
                    question: "एक समांतर चतुर्भुज का क्षेत्रफल का सूत्र क्या है?",
                   options: ["आधार × ऊंचाई", "लंबाई × चौड़ाई", "1/2 × आधार × ऊंचाई", "4 × भुजा"],
                    correctAnswer: "आधार × ऊंचाई"
                 },
                {
                    question: "यदि cosθ = 1/2, तो θ का मान क्या है?",
                   options: ["30 डिग्री", "45 डिग्री", "60 डिग्री", "90 डिग्री"],
                    correctAnswer: "60 डिग्री"
                },
                  {
                     question: "एक त्रिभुज का क्षेत्रफल का सूत्र क्या है?",
                   options: ["1/2 × आधार × ऊंचाई", "आधार × ऊंचाई", "लंबाई × चौड़ाई", "4 × भुजा"],
                     correctAnswer: "1/2 × आधार × ऊंचाई"
                 },
                  {
                   question: "यदि tanθ = 1, तो θ का मान क्या है?",
                   options: ["30 डिग्री", "45 डिग्री", "60 डिग्री", "90 डिग्री"],
                   correctAnswer: "45 डिग्री"
                   },
                    {
                    question: "2 का घन क्या है?",
                     options: ["4", "6", "8", "10"],
                     correctAnswer: "8"
                 },
                   {
                    question: "एक समबाहु त्रिभुज का प्रत्येक कोण कितने डिग्री का होता है?",
                    options: ["30", "45", "60", "90"],
                    correctAnswer: "60"
                }

            ],
            quiz2: [
                {
                    question: "समीकरण x² - 5x + 6 = 0 के मूल क्या हैं?",
                     options: ["(2, 3)", "(1, 6)", "(-2, -3)", "(2, -3)"],
                    correctAnswer: "(2, 3)"
                },
                 {
                     question: "यदि एक समांतर श्रेणी का पहला पद 5 और सामान्य अंतर 3 है, तो 10वां पद क्या होगा?",
                      options: ["29", "32", "35", "38"],
                     correctAnswer: "32"
                },
                 {
                     question: "बिंदु (2, 3) और (4, 7) को मिलाने वाली रेखा का मध्यबिंदु क्या है?",
                    options: ["(3, 5)", "(2, 5)", "(4, 6)", "(5, 4)"],
                     correctAnswer: "(3, 5)"
                },
                 {
                     question: "sin²θ + cos²θ का मान क्या है?",
                     options: ["0", "1", "2", "3"],
                    correctAnswer: "1"
                },
                {
                     question: "एक लंबवृत्तीय शंकु के वक्र पृष्ठीय क्षेत्रफल का सूत्र क्या है?",
                   options: ["πrl", "2πrl", "πr²l", "4πrl"],
                    correctAnswer: "πrl"
                 },
                {
                    question: "एक बेलन का कुल पृष्ठीय क्षेत्रफल का सूत्र क्या है?",
                   options: ["2πr(r+h)", "πr²h", "πrl", "2πrh"],
                     correctAnswer: "2πr(r+h)"
                },
                {
                    question: "10, 14, 18, 22,... का 20वां पद क्या है?",
                   options: ["98", "114", "102", "106"],
                    correctAnswer: "106"
                },
                {
                    question: "2 + 4 + 6 + 8 + ... + 20 का योग क्या है?",
                    options: ["110", "100", "120", "130"],
                     correctAnswer: "110"
                },
                   {
                     question: "एक पासे को फेंकने पर 5 आने की प्रायिकता क्या है?",
                    options: ["1/6", "1/3", "1/2", "2/3"],
                    correctAnswer: "1/6"
                  },
                    {
                    question: "एक सिक्के को दो बार उछालने पर दोनों बार पट आने की प्रायिकता क्या है?",
                    options: ["1/2", "1/4", "1/8", "3/4"],
                     correctAnswer: "1/4"
                },
                    {
                    question: "एक अच्छी तरह से फेंटी हुई ताश की गड्डी से एक पत्ता निकालने पर लाल पत्ता आने की प्रायिकता क्या है?",
                     options: ["1/2", "1/4", "1/8", "3/4"],
                    correctAnswer: "1/2"
                },
                  {
                     question: "एक बहुपद p(x) के शून्यक क्या हैं यदि p(x) = x² - 4x + 3?",
                   options: ["1, 3", "-1, -3", "1, -3", "-1, 3"],
                     correctAnswer: "1, 3"
                },
                 {
                   question: "एक चतुर्भुज के सभी कोणों का योग कितना होता है?",
                   options: ["180°", "270°", "360°", "450°"],
                    correctAnswer: "360°"
                },
                 {
                     question: "यदि किसी समांतर चतुर्भुज का एक कोण 90° है, तो वह क्या है?",
                    options: ["आयत", "समचतुर्भुज", "वर्ग", "समलंब"],
                     correctAnswer: "आयत"
                },
                {
                     question: "एक वृत्त की सबसे बड़ी जीवा (chord) क्या है?",
                    options: ["त्रिज्या", "व्यास", "चाप", "स्पर्श रेखा"],
                    correctAnswer: "व्यास"
                },
                {
                    question: "यदि tan A = 3/4, तो sin A का मान क्या है?",
                    options: ["3/5", "4/5", "5/3", "5/4"],
                     correctAnswer: "3/5"
                  },
                {
                     question: "यदि एक लंबवृत्तीय बेलन की त्रिज्या 7 सेमी और ऊंचाई 10 सेमी है, तो उसका आयतन क्या है?",
                   options: ["1540 सेमी³", "154 सेमी³", "770 सेमी³", "2156 सेमी³"],
                    correctAnswer: "1540 सेमी³"
                },
                {
                    question: "यदि एक शंकु की त्रिज्या 3 सेमी और ऊँचाई 4 सेमी है, तो उसकी तिरछी ऊँचाई क्या है?",
                   options: ["5 सेमी", "7 सेमी", "9 सेमी", "12 सेमी"],
                     correctAnswer: "5 सेमी"
                  },
                {
                    question: "1, 4, 9, 16,... अनुक्रम में अगला पद क्या है?",
                     options: ["20", "25", "27", "30"],
                    correctAnswer: "25"
                },
                {
                    question: "एक रैखिक समीकरण का मानक रूप क्या है?",
                     options: ["ax + by = c", "ax^2 + bx + c = 0", "ax^3 + bx^2 + cx + d = 0", "ax^4 + bx^3 + cx^2 + dx + e = 0"],
                     correctAnswer: "ax + by = c"
                },
               {
                     question: "यदि एक वृत्त का व्यास 14 सेमी है, तो उसकी परिधि क्या होगी?",
                    options: ["22 सेमी", "44 सेमी", "88 सेमी", "154 सेमी"],
                     correctAnswer: "44 सेमी"
                 },
                 {
                    question: "दो रेखाएँ समांतर होती हैं यदि उनके ढाल क्या हों?",
                     options: ["समान", "विपरीत", "शून्य", "एक दूसरे के लंबवत"],
                     correctAnswer: "समान"
                 },
                {
                    question: "1 से 20 तक की संख्याओं में कितनी सम संख्याएँ हैं?",
                    options: ["5", "10", "12", "15"],
                    correctAnswer: "10"
                  },
                 {
                    question: "1 से 20 तक की संख्याओं में कितनी विषम संख्याएँ हैं?",
                    options: ["5", "10", "12", "15"],
                     correctAnswer: "10"
                   },
                {
                   question: "6, 8 और 10 का लघुत्तम समापवर्त्य क्या है?",
                    options: ["60", "120", "240", "180"],
                     correctAnswer: "120"
               }

            ],
             quiz3: [
                    {
                    question: "यदि sec θ = 2, तो cos θ का मान क्या है?",
                     options: ["1/2", "2", "√3/2", "1/√2"],
                    correctAnswer: "1/2"
                },
                {
                    question: "यदि cot θ = 1, तो tan θ का मान क्या है?",
                    options: ["0", "1", "2", "1/2"],
                     correctAnswer: "1"
                 },
                {
                    question: "एक आयत का परिमाप का सूत्र क्या है?",
                    options: ["लंबाई + चौड़ाई", "2(लंबाई + चौड़ाई)", "लंबाई × चौड़ाई", "4 × भुजा"],
                     correctAnswer: "2(लंबाई + चौड़ाई)"
                },
                {
                    question: "एक वर्ग का परिमाप का सूत्र क्या है?",
                   options: ["4 × भुजा", "2 × भुजा", "भुजा^2", "भुजा^3"],
                    correctAnswer: "4 × भुजा"
                },
                {
                     question: "एक समबाहु त्रिभुज का क्षेत्रफल का सूत्र क्या है?",
                     options: ["√3/4 भुजा^2", "1/2 × आधार × ऊंचाई", "भुजा^2", "4 × भुजा"],
                    correctAnswer: "√3/4 भुजा^2"
                 },
                {
                     question: "यदि एक वृत्त का क्षेत्रफल 616 वर्ग सेमी है, तो उसकी त्रिज्या क्या होगी?",
                    options: ["7 सेमी", "14 सेमी", "21 सेमी", "28 सेमी"],
                    correctAnswer: "14 सेमी"
                },
                {
                     question: "एक घनाभ में कितने किनारे होते हैं?",
                    options: ["6", "8", "12", "10"],
                   correctAnswer: "12"
                },
                {
                    question: "एक घन में कितने फलक होते हैं?",
                    options: ["4", "6", "8", "12"],
                    correctAnswer: "6"
                },
                 {
                    question: "25 और 30 का महत्तम समापवर्तक (HCF) क्या है?",
                    options: ["5", "10", "15", "25"],
                     correctAnswer: "5"
                },
                  {
                    question: "30 और 45 का लघुत्तम समापवर्त्य (LCM) क्या है?",
                   options: ["45", "60", "90", "120"],
                     correctAnswer: "90"
                 },
                {
                     question: "दो समांतर रेखाओं के बीच की दूरी कैसी रहती है?",
                   options: ["कम होती है", "बढ़ती है", "समान रहती है", "बदलाव होता है"],
                     correctAnswer: "समान रहती है"
                 },
                 {
                   question: "एक समांतर चतुर्भुज के सम्मुख कोण कैसे होते हैं?",
                   options: ["बराबर", "पूरक", "पूरक", "आधे"],
                     correctAnswer: "बराबर"
                   },
                 {
                   question: "एक वृत्त की स्पर्श रेखा वृत्त को कितने बिंदुओं पर काटती है?",
                    options: ["एक", "दो", "तीन", "कोई नहीं"],
                    correctAnswer: "एक"
                 },
                 {
                    question: "एक वृत्त में कितने व्यास होते हैं?",
                    options: ["एक", "दो", "असीमित", "कोई नहीं"],
                     correctAnswer: "असीमित"
                   },
                 {
                     question: "एक असंभव घटना की प्रायिकता क्या होती है?",
                     options: ["0", "1", "1/2", "अनंत"],
                     correctAnswer: "0"
                },
                {
                    question: "एक निश्चित घटना की प्रायिकता क्या होती है?",
                   options: ["0", "1", "1/2", "अनंत"],
                    correctAnswer: "1"
                 },
                 {
                     question: "एक त्रिभुज का क्षेत्रफल 20 वर्ग सेमी है और आधार 8 सेमी है। ऊँचाई कितनी है?",
                   options: ["5 सेमी", "8 सेमी", "10 सेमी", "20 सेमी"],
                    correctAnswer: "5 सेमी"
                 },
                  {
                     question: "यदि a = 5 और b = 7, तो 2a + 3b का मान क्या होगा?",
                     options: ["21", "23", "29", "31"],
                     correctAnswer: "31"
                },
                {
                     question: "यदि 3x - 6 = 0, तो x का मान क्या होगा?",
                     options: ["0", "1", "2", "3"],
                     correctAnswer: "2"
                 },
                {
                    question: "यदि x/2 = 5, तो x का मान क्या होगा?",
                   options: ["5", "10", "2.5", "7"],
                    correctAnswer: "10"
                 },
                 {
                   question: "x² + 4x + 4 का गुणनखंड क्या है?",
                     options: ["(x+2)(x-2)", "(x+2)(x+2)", "(x-2)(x-2)", "(x+4)(x+1)"],
                    correctAnswer: "(x+2)(x+2)"
                 },
                 {
                    question: "एक लंबवृत्तीय बेलन में कितने वृत्ताकार सिरे होते हैं?",
                   options: ["एक", "दो", "तीन", "चार"],
                     correctAnswer: "दो"
                 },
                 {
                    question: "एक समलंब चतुर्भुज का क्षेत्रफल का सूत्र क्या है?",
                   options: ["1/2 × (समांतर भुजाओं का योग) × ऊँचाई", "आधार × ऊंचाई", "लंबाई × चौड़ाई", "4 × भुजा"],
                     correctAnswer: "1/2 × (समांतर भुजाओं का योग) × ऊँचाई"
                 },
                 {
                    question: "3, 5, 7, 9,... श्रृंखला का अगला पद क्या है?",
                     options: ["10", "11", "12", "13"],
                     correctAnswer: "11"
                },
                 {
                     question: "एक बेलन का वक्र पृष्ठ क्षेत्रफल का सूत्र क्या है?",
                    options: ["πr²h", "2πrh", "πrl", "4πr²"],
                    correctAnswer: "2πrh"
                 }

            ],
            quiz4: [
                    {
                   question: "100, 105, 110, 115,... का सामान्य अंतर क्या है?",
                    options: ["2", "5", "10", "15"],
                    correctAnswer: "5"
                  },
                    {
                    question: "एक लंबवृत्तीय शंकु के कुल पृष्ठीय क्षेत्रफल का सूत्र क्या है?",
                     options: ["πr(l+r)", "πrl", "πr²", "2πr²"],
                    correctAnswer: "πr(l+r)"
                },
                {
                    question: "यदि एक वृत्त का व्यास 10 सेमी है, तो उसकी त्रिज्या क्या होगी?",
                    options: ["5 सेमी", "10 सेमी", "15 सेमी", "20 सेमी"],
                     correctAnswer: "5 सेमी"
                },
                 {
                    question: "एक घन का विकर्ण का सूत्र क्या है?",
                    options: ["√3 × भुजा", "√2 × भुजा", "भुजा²", "2 × भुजा"],
                     correctAnswer: "√3 × भुजा"
                 },
                 {
                     question: "यदि दो त्रिभुज समरूप हैं, तो उनके संगत कोण कैसे होंगे?",
                    options: ["बराबर", "पूरक", "विपरीत", "आधे"],
                    correctAnswer: "बराबर"
                },
                {
                     question: "यदि दो त्रिभुजों की संगत भुजाएँ समानुपातिक हैं, तो त्रिभुज कैसे होंगे?",
                     options: ["समरूप", "सर्वांगसम", "बराबर", "अलग"],
                    correctAnswer: "समरूप"
                 },
                 {
                    question: "बिंदु (3, -2) किस चतुर्थांश में स्थित है?",
                    options: ["प्रथम", "द्वितीय", "तृतीय", "चतुर्थ"],
                    correctAnswer: "चतुर्थ"
                 },
                {
                     question: "बिंदु (-2, -3) किस चतुर्थांश में स्थित है?",
                     options: ["प्रथम", "द्वितीय", "तृतीय", "चतुर्थ"],
                    correctAnswer: "तृतीय"
                 },
                  {
                    question: "एक अर्धगोले का आयतन का सूत्र क्या है?",
                    options: ["2/3πr³", "4/3πr³", "πr²h", "πrl"],
                     correctAnswer: "2/3πr³"
                },
                 {
                     question: "एक अर्धगोले का वक्र पृष्ठीय क्षेत्रफल का सूत्र क्या है?",
                    options: ["2πr²", "4πr²", "πr²", "2πrh"],
                    correctAnswer: "2πr²"
                },
                 {
                     question: "एक वर्ग में कितने समकोण होते हैं?",
                   options: ["2", "4", "6", "8"],
                    correctAnswer: "4"
                 },
                 {
                   question: "एक समकोण त्रिभुज में सबसे बड़ी भुजा को क्या कहते हैं?",
                     options: ["आधार", "लंब", "कर्ण", "मध्यिका"],
                   correctAnswer: "कर्ण"
                 },
                 {
                     question: "2, 4, 8, 16,... श्रृंखला में अगला पद क्या है?",
                   options: ["24", "32", "40", "48"],
                    correctAnswer: "32"
                 },
                {
                    question: "एक समांतर श्रेणी में, यदि प्रथम पद 'a' और सामान्य अंतर 'd' है, तो nवें पद का सूत्र क्या है?",
                     options: ["a + nd", "a + (n-1)d", "an + d", "a - (n-1)d"],
                    correctAnswer: "a + (n-1)d"
                 },
                {
                     question: "यदि a = 2, b = 3, और c = 4, तो a + b - c का मान क्या होगा?",
                    options: ["1", "2", "3", "4"],
                     correctAnswer: "1"
                 },
                  {
                     question: "यदि p(x) = x² - 5x + 6, तो p(2) का मान क्या होगा?",
                    options: ["0", "1", "2", "3"],
                     correctAnswer: "0"
                 },
                   {
                    question: "यदि cos A = 4/5, तो sec A का मान क्या है?",
                     options: ["3/5", "4/5", "5/4", "5/3"],
                    correctAnswer: "5/4"
                 },
                {
                    question: "यदि sin A = 3/5, तो cosec A का मान क्या है?",
                    options: ["3/5", "4/5", "5/3", "5/4"],
                    correctAnswer: "5/3"
                 },
                  {
                    question: "एक वृत्त की त्रिज्या 7 सेमी है, तो उसका व्यास क्या होगा?",
                   options: ["7 सेमी", "14 सेमी", "21 सेमी", "28 सेमी"],
                     correctAnswer: "14 सेमी"
                },
                   {
                    question: "एक वृत्त के परिधि और व्यास का अनुपात क्या होता है?",
                    options: ["π/2", "π", "2π", "4π"],
                    correctAnswer: "π"
                  },
                   {
                     question: "एक बहुभुज जिसके सभी कोण और भुजाएँ बराबर हों, उसे क्या कहते हैं?",
                    options: ["सम बहुभुज", "विषम बहुभुज", "त्रिकोण", "चतुर्भुज"],
                    correctAnswer: "सम बहुभुज"
                 },
                {
                    question: "1, 1, 2, 3, 5, 8,... श्रृंखला में अगला पद क्या है?",
                     options: ["11", "12", "13", "14"],
                    correctAnswer: "13"
                 },
                {
                     question: "यदि एक रेखा X-अक्ष के समांतर है, तो उसका ढाल क्या होगा?",
                    options: ["0", "1", "अनंत", "-1"],
                     correctAnswer: "0"
                 },
                  {
                   question: "यदि एक रेखा Y-अक्ष के समांतर है, तो उसका ढाल क्या होगा?",
                     options: ["0", "1", "अनंत", "-1"],
                     correctAnswer: "अनंत"
                 },
                 {
                    question: "यदि दो रेखाएँ एक दूसरे के लंबवत हैं, तो उनके ढाल का गुणनफल क्या होगा?",
                    options: ["0", "1", "-1", "2"],
                     correctAnswer: "-1"
                 }
            ]
        };

    const tabs = document.querySelectorAll('.tab');
    const tabContents = document.querySelectorAll('.tab-content');
    const quizContainer = document.querySelector('.quiz-container')
     let activeQuiz ='quiz1';
      let participants = [];
        function loadQuiz(quizId){
         let quizForm = document.getElementById(quizId);
         quizForm.innerHTML = '';
         const currentQuiz = questions[quizId];
         if (!currentQuiz) return;
          currentQuiz.forEach((question, index)=>{
            let questionHTML = `
                  <section class="question">
                        <h2>प्रश्न ${index + 1}:</h2>
                        <p>${question.question}</p>
                         <div class="options">`
                   question.options.forEach((option)=>{
                       questionHTML +=  `<label><input type="radio" name="q${index}" value="${option}"> ${option}</label>`
                   })
                    questionHTML += ` </div> </section>`
             quizForm.innerHTML += questionHTML;
            });
             quizForm.innerHTML += `<button type="submit">जमा करें</button>`;

             quizForm.addEventListener('submit', function(event){
                 event.preventDefault();
                 const userAnswers = {};
                   let score = 0;
                    currentQuiz.forEach((question, index) =>{
                       userAnswers[`q${index}`] = document.querySelector(`input[name="q${index}"]:checked`)?.value;
                       if(userAnswers[`q${index}`] === question.correctAnswer){
                          score++;
                       }
                    });

                    let resultsHTML = `<h2>परिणाम (क्विज़ ${quizId.slice(-1)}):</h2>`;
                     currentQuiz.forEach((question, index)=>{
                         const userAnswer = userAnswers[`q${index}`];
                         if(userAnswer === question.correctAnswer){
                           resultsHTML += `<p><b>प्रश्न ${index+1}:</b> <span class="correct">सही</span>, सही उत्तर: ${question.correctAnswer}</p>`;
                         } else {
                           resultsHTML += `<p><b>प्रश्न ${index+1}:</b> <span class="incorrect">गलत</span>, आपका उत्तर: ${userAnswer || 'कोई उत्तर नहीं'}, सही उत्तर: ${question.correctAnswer}</p>`;
                         }
                     });
                    resultsHTML += `<p>कुल अंक: ${score} / ${currentQuiz.length}</p>`;
                    document.getElementById('results').innerHTML = resultsHTML;
                   document.getElementById('results').style.display = 'block';
                  updateParticipants(score,quizId);

            });
    }
     tabs.forEach(tab => {
            tab.addEventListener('click', () => {
                tabs.forEach(t => t.classList.remove('active'));
                  tabContents.forEach(content => content.classList.remove('active'));
                tab.classList.add('active');
                const tabId = tab.getAttribute('data-tab');
                  document.getElementById(tabId).classList.add('active');
                loadQuiz(tabId);
                activeQuiz = tabId;
            });
        });
      loadQuiz(activeQuiz)
        function updateParticipants(score,quizId){

            const participantName = prompt('अपना नाम दर्ज करें:');
            if (participantName){
                 participants.push({ name: participantName, score: score, quiz: quizId });
            }
        let participantsHTML = '<h2>प्रतिभागियों</h2><ul>';
         participants.forEach(participant => {
             participantsHTML += `<li>${participant.name} - Score: ${participant.score} - Quiz: ${participant.quiz.slice(-1)}</li>`
         });
          participantsHTML += '</ul>'
           document.getElementById('participants').innerHTML = participantsHTML;
           document.getElementById('participants').style.display = 'block';

        }
    </script>
</body>
</html>