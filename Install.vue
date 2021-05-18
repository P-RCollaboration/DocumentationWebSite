<template>
    <div class="introduction-container">
        <span class="main-header-title">
            Install
        </span>
        <span class="main-subheader-title">
            Provue is component set it is not library is because you can use any part of it separately.            
        </span>
        <span class="main-accentheader-title">
            Vue.js
        </span>
        <span>
            For work with Provue you need first install <a href="https://vuejs.org/">Vue.js</a>.
            Currently supported Vue.js 2 and 3.
        </span>
        <span>
            You can install vue via npm:
        </span>
        <span>
            For Vue.js 2
        </span>
        <div class="code-section">            
            <span>&gt; npm i vue</span>
        </div>
        <span>
            For Vue.js 3
        </span>
        <div class="code-section">            
            <span>&gt; npm i vue@next</span>
        </div>
        <span>
            or via cdn:
        </span>
        <span>
            For Vue.js 2
        </span>
        <div class="code-section">
            <span>&lt;script src="https://cdn.jsdelivr.net/npm/vue@2.6.12"&gt;&lt;/script&gt;</span>
        </div>
        <span>
            For Vue.js 3
        </span>
        <div class="code-section">
            <span>&lt;script src="https://unpkg.com/vue@next"&gt;&lt;/script&gt;</span>
        </div>
        <span class="main-accentheader-title">
            Bootstraper and dependency resolver
        </span>
        <span>
            Bootstraper contains functionality for simplification loading component dynamically.
        </span>
        <span class="code-section">
            <span>&lt;script src="https://p-rcollaboration.github.io/CoreComponents/src/libraries/vuejs.bootstraper.js"&gt;&lt;/script&gt;</span>
        </span>
        <span>
            Dependency resolver it library for loading scripts and styles
        </span>
        <span class="code-section">
            <span>&lt;script src="https://p-rcollaboration.github.io/CoreComponents/src/libraries/resolveDependencies.js"&gt;&lt;/script&gt;</span>
        </span>
        <span>
            Bind dependency resolver and bootstraper
        </span>
        <span class="code-section">
            VueBootstraper.require = DependencyResolver;
        </span>
    </div>
</template>

<script>
export default {
    name: `Introduction`
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