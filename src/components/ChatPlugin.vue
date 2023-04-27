<template>
    <div id="rasa-chat-widget" data-websocket-url="https://f534-43-242-224-42.in.ngrok.io" data-avatar-url="https://icon2.cleanpng.com/20171220/xxq/smiley-png-5a3a6ae39e2dd7.0296809115137778916479.jpg"></div>
</template>

<script>
export default{
    name: 'ChatPlugin',
    data:()=>({
        // connUrl: "http://localhost:5005",
        // avatarUrl: "../assets/img/bot-logo.png",
    }),
    mounted() {
      let recaptchaScript = document.createElement('script')
      recaptchaScript.setAttribute('src', 'https://unpkg.com/@rasahq/rasa-chat')
      document.head.appendChild(recaptchaScript)
    },
}
</script>