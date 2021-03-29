<template>
    <div class="introduction-container">
        <span class="main-header-title">
            Introduction
        </span>
        <span class="main-subheader-title">
            Getting started with a flexible component set Provue for rapid development complex feature-rich UI for modern Web.
        </span>
        <span class="main-accentheader-title">
            Micro frontend or monolith?
        </span>
        <span>
            Micro Frontends
            <a href="https://micro-frontends.org/">(link)</a>
            it new area in frontend development that aim to split frontend in small parts.
            Ideally, parts have to be fully isolated apart but it not easy because the application can have common environment options, css and so on.
            Of course, also can have issues with routing and intercommunication between small parts.
            But all issues can be solved and at end of the day, you can get the opportunity to separate your monolith frontend between teams and increase pace development.
            <br />
            Our goal tries to solve as many as possible issues related to Micro Frontends with a component set Provue.
            As a foundation, we decided to select the library Vue.js.
            Single File Component that Vue.js suggest it our opition ideal fit for implement Micro Frontends because all parts - template, css, script and required dependencies defined in one file.
            Components have flexible parent-children communication methods.
            Children's components can be lazy-loaded.
        </span>
        <span class="main-accentheader-title">
            Component separation
        </span>
        <span>
            As you know from previous section Micro Frontends have few issues that need to be solved. One from that issues will be solved way separate
            all components on two parts - state and view.
            State keeps logic and state using as controller (in terms MVC). View keeps methods for drawing html.
            Why it need it separation? As nature Micro Frontends keep thing small separated. Idea behind separation that you can use "common components" with
            same api but you feel free change it visual representation in different small parts of you application.
        </span>
        <span class="main-accentheader-title">
            Quick start
        </span>
        <span>
            By tradition, first create a folder for the project
        </span>
        <div class="code-section">
            <span>&gt; mkdir testfolder</span>
            <span>&gt; cd testfolder</span>
        </div>
        <span>
            You need static server. As instance I will be use package http-server from npm.
            <br />All what you need it run command:
        </span>
        <div class="code-section">
            > npm install http-server -g
        </div>
        <span>
            After it you need create <b>index.html</b> file:
        </span>
        <iframe
            src="https://pastebin.com/embed_iframe/SU7Lf8dD"
            class="hello-world-example">
        </iframe>
        <span>
            and create component file <b>App.vue</b>
        </span>
        <iframe
            src="https://pastebin.com/embed_iframe/xffByPK2"
            class="hello-world-example">
        </iframe>
        <span>
            Final step, run static server:
        </span>
        <div class="code-section">
            > http-server -a localhost -p 8080
        </div>
        <span>
            Check it out in <a href="http://localhost:8080">browser</a>.
        </span>
    </div>
</template>

<script>
export default async function () {
    return {
        name: `Introduction`,
        methods: {
        },
        components: {
        }
    }
}
</script>

<style>
.introduction-container {
    display: flex;
    flex-direction: column;
}
.hello-world-example {
    border: none;
    width: 100%;
    height: 400px;
    margin: 20px;
}
</style>