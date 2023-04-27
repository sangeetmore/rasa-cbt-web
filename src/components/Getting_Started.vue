<template>
<div id="get-started" class="dark-bg">
    <br />
    <h1 class="text-center text-white">
        Getting <span class="primary-color">Started</span>
    </h1>
    <br />
    <br />

    <div class="container">
        <h3 data-aos="fade-right" data-aos-duration="500" class="text-white text-center">
            To test our bot, click on the dialog box on the right!
            <!-- <span class="primary-color">&lt;link&gt;</span>  -->
            <!-- <span class="primary-color">&lt;head&gt;</span>  -->
        </h3>
        <br />

        <!-- <pre class="language-javascript"> -->
            <!-- <div class="copy">Copy</div> -->
            <!-- <code class="language-js language-markup">     
                &lt;link rel="stylesheet" href="https://drive.google.com/uc?id=1x2TCnJdXTQFErgZhxjMUWKIIfIfSbIy-">
            </code> -->
        <!-- </pre> -->

        <br />

        <h3 data-aos="fade-right" data-aos-duration="500" class="text-white text-center">
            You can also visit our<a href="https://github.com/sangeetmore/headspace-helper"> <svg xmlns="http://www.w3.org/2000/svg" height="50" width="50" data-name="Layer 1" viewBox="0 0 24 24" id="github"><path d="M12,2.2467A10.00042,10.00042,0,0,0,8.83752,21.73419c.5.08752.6875-.21247.6875-.475,0-.23749-.01251-1.025-.01251-1.86249C7,19.85919,6.35,18.78423,6.15,18.22173A3.636,3.636,0,0,0,5.125,16.8092c-.35-.1875-.85-.65-.01251-.66248A2.00117,2.00117,0,0,1,6.65,17.17169a2.13742,2.13742,0,0,0,2.91248.825A2.10376,2.10376,0,0,1,10.2,16.65923c-2.225-.25-4.55-1.11254-4.55-4.9375a3.89187,3.89187,0,0,1,1.025-2.6875,3.59373,3.59373,0,0,1,.1-2.65s.83747-.26251,2.75,1.025a9.42747,9.42747,0,0,1,5,0c1.91248-1.3,2.75-1.025,2.75-1.025a3.59323,3.59323,0,0,1,.1,2.65,3.869,3.869,0,0,1,1.025,2.6875c0,3.83747-2.33752,4.6875-4.5625,4.9375a2.36814,2.36814,0,0,1,.675,1.85c0,1.33752-.01251,2.41248-.01251,2.75,0,.26251.1875.575.6875.475A10.0053,10.0053,0,0,0,12,2.2467Z">/a></path></svg></a>
            
        </h3>

        <br />

        <h4 data-aos="fade-right" data-aos-duration="500" class="text-white text-center">
            Create a virtual environment in python.
            Run the commands for testing the chatbot after cloning the repository from GitHub.
        </h4>
        
        <!-- <div class="copy">Copy</div> -->
        
        <pre class="language-js">
        <code class="language-js">     
                pip3 install rasa
                rasa train
                rasa shell
            </code>
        </pre>

        <!-- <div class="row">
            <div class="col-12 col-sm-12 col-md-12 col-lg-6 col-xl-6">
                <ul class="list-group list-group-left">

                <li data-aos="fade-right" :data-aos-duration="obj.duration" class="list-group-item list-group-item-left" v-for="(obj, key) in left_cards" :key="key">
                        <b class="arrow">>></b>
                        <span class="title">{{obj.title}}: </span>{{obj.description}}
                    </li>
                   
                </ul>
            </div>

            <div class="col">
                <ul class="list-group list-group-right">
                <li data-aos="fade-left" :data-aos-duration="obj.duration" class="list-group-item list-group-item-left" v-for="(obj, key) in right_cards" :key="key">
                        <b class="arrow">>></b>
                        <span class="title">{{obj.title}}: </span>{{obj.description}}
                    </li>
                   
                </ul>
            </div>
        </div> -->
    </div>
</div>
</template>

<script>
import Prism from 'prismjs'
import Clipboard from 'clipboard'
// import 'prismjs/themes/prism-okaidia.css'
import '../assets/css/prism.css'

import 'prismjs/components/prism-javascript'
import 'prismjs/components/prism-markdown'
import 'prismjs/components/prism-markup-templating'

// create clipboard for every copy element
const clipboard = new Clipboard('.copy', {
  target: (trigger) => {
    return trigger.nextElementSibling;
  }
});


// do stuff when copy is clicked
clipboard.on('success', (event) => {
  event.trigger.textContent = 'Copied!';
  setTimeout(() => {
    event.clearSelection();
    event.trigger.textContent = 'Copy';
  }, 1000);
});



export default {
    name: "Getting_Started",

    data: () => ({
        left_cards : [
            {
                duration:"500",
                title:"createChatbot",
                description:"To initailize & set various aspects of chatbot"
            },
            {
                duration:"700",
                title:"host",
                description:"The URL of hosted chatbot"
            },
            {
                duration:"850",
                title:"botLogo",
                description:"Logo Of the Bot"
            },
            {
                duration:"1000",
                title:"title",
                description:"The title which will appear on the header of chatbot"
            },
        ],

        right_cards : [
            {
                duration:"600",
                title:"welcomeMessage",
                description:"Starting Message shown to the user, can be any greeting or information"
            },
            {
                duration:"750",
                title:"inactiveMsg",
                description:"When bot server is down or unreachable this message will be shown"
            },
            {
                duration:"900",
                title:"theme",
                description:"Color of header, bot message and overall layout, there are two inbuilt theme for bot, blue and purple"
            },
            
        ]
    }),

    mounted() {
        Prism.highlightAll()
    }

};
</script>

<style>
#get-started {
    overflow-x: hidden;
}

@media (max-width: 768px) {
    body {
        overflow-x: hidden
    }
}
</style>
