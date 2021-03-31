<template>
    <div class="loading-components-container">
        <span class="main-header-title">
            Loading Components
        </span>
        <span class="main-subheader-title">
            Provue have few methods for loading components. Below describe each from it.
        </span>
        <span class="main-accentheader-title">
            How to use it externally
        </span>
        <div class="code-section">
            <span>
                // if you use bundlers<br />
                import Vue2Bootstraper from `../vuejs2bootstraper.js`<br />
                // or if you load directly<br />
                &lt;script src='...'&gt;&lt;/script&gt;<br />
                <br />
                new Vue(<br />
                &nbsp;&nbsp;{<br />
                &nbsp;&nbsp;&nbsp;&nbsp;el: `#app`,<br />
                &nbsp;&nbsp;&nbsp;&nbsp;template: `&lt;app&gt;&lt;/app&gt;`,<br />
                &nbsp;&nbsp;&nbsp;&nbsp;components: {<br />
                &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span class="highlighted-text">App: () => Vue2Bootstraper.loadComponent(`App.vue`)</span><br />
                &nbsp;&nbsp;&nbsp;&nbsp;}<br />
                &nbsp;&nbsp;}<br />
                );<br />
            </span>
        </div>
        <span class="main-accentheader-title">
            How to load component dynamically
        </span>
        <span>
            It fit if components often changing or creating dynamically.
        </span>
        <div class="code-section">
            <span>
                <br />
                export default async function () {<br />
                &nbsp;&nbsp;<span class="highlighted-text">const DynamicComponent = await loadComponent(`../DynamicComponent.vue`);</span><br /><br />
                &nbsp;&nbsp;return {<br />
                &nbsp;&nbsp;&nbsp;&nbsp;name: `Test`,<br />
                &nbsp;&nbsp;&nbsp;&nbsp;components: {<br />
                &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span class="highlighted-text">DynamicComponent</span><br />
                &nbsp;&nbsp;&nbsp;&nbsp;}<br />
                &nbsp;&nbsp;}<br />
                );<br />
            </span>
        </div>
        <span class="main-accentheader-title">
            How to load component global
        </span>
        <span>
            It fits if your components simple static files. Usually convenient to define global components in one place on top of the component's root. After it, you can use the global component in the template in all components without definition in the components section.
        </span>
        <div class="code-section">
            <span>
                &lt;template&gt;<br />
                &nbsp;&nbsp;&lt;static-component&gt;&lt;/static-component&gt;<br />
                &lt;/template&gt;<br />
                <br />
                export default async function () {<br />
                &nbsp;&nbsp;<span class="highlighted-text">await globalComponent(`../StaticComponent.vue`);</span><br /><br />
                &nbsp;&nbsp;return {<br />
                &nbsp;&nbsp;&nbsp;&nbsp;name: `Test`<br />
                &nbsp;&nbsp;}<br />
                );<br />
            </span>
        </div>
    </div>
</template>

<script>
export default {
    name: `LoadingComponents`
}
</script>

<style>
.loading-components-container {
    display: flex;
    flex-direction: column;
}
</style>