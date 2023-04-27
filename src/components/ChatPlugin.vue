<template>
    <div id="rasa-chat-widget" data-websocket-url="" data-avatar-url="https://icon2.cleanpng.com/20171220/xxq/smiley-png-5a3a6ae39e2dd7.0296809115137778916479.jpg"></div>
</template>

<script>
import CONSTANTS from '../constants/constants';
export default{
    name: 'ChatPlugin',
    data:()=>({
        connUrl: CONSTANTS.connUrl,
    }),
    mounted() {
      let recaptchaScript = document.createElement('script')
      recaptchaScript.setAttribute('src', 'https://unpkg.com/@rasahq/rasa-chat')
      document.head.appendChild(recaptchaScript)
    },
}
</script>