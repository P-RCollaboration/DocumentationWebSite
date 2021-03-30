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
            Currently supported only Vue.js 2.6.0+. Supporting Vue.js 3 is coming soon.
        </span>
        <span>
            You can install vue via npm:
        </span>
        <div class="code-section">
            <span>&gt; npm i vue</span>
        </div>
        <span>
            or via cdn:
        </span>
        <div class="code-section">
            <span>&lt;script src="https://cdn.jsdelivr.net/npm/vue@2.6.12"&gt;&lt;/script&gt;</span>
        </div>
        <span class="main-accentheader-title">
            Bootstraper and dependency 
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