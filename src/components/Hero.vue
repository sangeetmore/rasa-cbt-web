<template>
<div class="hero" id="hero">

    <nav class="navbar navbar-expand-lg navbar-light">
        <div class="container">
            <a class="navbar-brand" href="#hero"><i class="fas fa-microchip-ai"></i> Headspace <span>Helper</span>
            </a>
            <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
                <span class="navbar-toggler-icon"></span>
            </button>
            <div class="collapse navbar-collapse" id="navbarSupportedContent">
                <ul class="navbar-nav ml-auto">
                    <li class="nav-item">
                        <a class="nav-link text-white hover" href="#features">Features</a>
                    </li>
                    <li class="nav-item active">
                        <a class="nav-link text-white font-weight-bold hover" href="#get-started">Get Started</a>
                    </li>
                    <!-- <li class="nav-item"> -->
                        <!-- <a class="nav-link text-white hover" href="#themes-and-upgrades">Themes And Upgrades</a> -->
                    <!-- </li> -->
                    <li class="nav-item">
                        <a class="nav-link text-white hover" target="_blank" href=" https://github.com/sangeetmore/headspace-helper">Repo</a>
                    </li>
                </ul>
            </div>
        </div>
    </nav>

    <br />

    <div class="hero-content">
        <div class="hero-bot mobile">
            <img src="../assets/img/cbt-img.png" alt="Bot Image" />
        </div>

        <div data-aos="fade-down-right" data-aos-duration="1000" class="hero-header" style="margin-top: 12rem;">
            <h1>Chat Your Way to Mental Wellness:<br><span class="primary-color"> Introducing Our Mental Health Chatbot</span><br></h1>

            <br />
            <p>
                Our chatbot is designed to provide you with a safe and supportive space to talk about your mental health concerns. Whether you're struggling with anxiety, depression, or any other mental health issue, our chatbot is here to help.
            </p>

            <br>
            <h3><span class="primary-color">Test our bot by clicking the icon on the bottom-right!</span></h3>

            <!-- <div class="btns"> -->
                <!-- <a href="#get-started"><button class="btn-green">Get Started</button></a> -->
                <!-- <button @click="downloadFile" class="btn-green">Download</button> -->
            <!-- </div> -->
        </div>

        <div data-aos="fade-up-left" data-aos-duration="1000" class="hero-bot desktop">
            <img src="../assets/img/cbt-img.png" alt="Bot Image" />
        </div>
    </div>
    <br>

</div>
</template>

<script>
import "../assets/css/styles.css";

import axios from "axios"

export default {
    name: "Hero",

    methods: {
        downloadFile() {
            axios({
                url: "http://localhost:8081/Chatbot-UI.zip",
                method: 'GET',
                responseType: 'blob'
            }).then((response) => {
                var fileUrl = window.URL.createObjectURL(new Blob([response.data]))
                var fileLink = document.createElement('a')
                fileLink.href = fileUrl

                fileLink.setAttribute("download", "Chatbot-UI.zip")
                document.body.appendChild(fileLink)
                fileLink.click()
            })

        }
    },
};
</script>

<style>
#hero {
    overflow-x: hidden;
}

@media (max-width: 768px) {
    body {
        overflow-x: hidden
    }
}
</style>
