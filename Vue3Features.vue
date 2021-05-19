<template>
    <div class="vue3features-container">
        <span class="main-header-title">
            How to use Vue.js 3 features (like Composition api ans so on)?
        </span>
        <span class="main-subheader-title">
            Many Vue.js 3 features a contains in vue module and created Vue application. But how to get reference to it?
        </span>
        <span class="main-accentheader-title">
            Vue Application 
        </span>
        <span>
            Application instance it that what you are created by <b>Vue.createApp(...)</b> method.
        </span>
        <span>
            Inside components, you can use <b>vueApplication</b> to get access to Vue application.
        </span>
        <div>
            <div style="color: rgb(212, 212, 212); background-color: rgb(30, 30, 30); font-family: Consolas, &quot;Courier New&quot;, monospace; font-size: 14px; line-height: 19px; white-space: pre;"><div><span style="color: rgb(128, 128, 128);">&lt;</span><span style="color: rgb(86, 156, 214);">script</span><span style="color: rgb(128, 128, 128);">&gt;</span></div><div><span style="color: rgb(197, 134, 192);">export</span>&nbsp;<span style="color: rgb(197, 134, 192);">default</span>&nbsp;{</div><div>&nbsp;&nbsp;&nbsp;&nbsp;<span style="color: rgb(156, 220, 254);">name:</span>&nbsp;<span style="color: rgb(206, 145, 120);">`TestComponent`</span>,</div><div>&nbsp;&nbsp;&nbsp;&nbsp;<span style="color: rgb(156, 220, 254);">methods:</span>&nbsp;{</div><div>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span style="color: rgb(220, 220, 170);">interactionWithApplication</span>()&nbsp;{</div><div>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span style="color: rgb(106, 153, 85);">//&nbsp;global&nbsp;register&nbsp;new&nbsp;component&nbsp;in&nbsp;application</span></div><div>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span style="color: rgb(156, 220, 254);">vueApplication</span>.<span style="color: rgb(220, 220, 170);">component</span>(<span style="color: rgb(206, 145, 120);">`new-test-component`</span>,&nbsp;{});</div><div>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;}</div><div>&nbsp;&nbsp;&nbsp;&nbsp;}</div><div>}</div><div><span style="color: rgb(128, 128, 128);">&lt;/</span><span style="color: rgb(86, 156, 214);">script</span><span style="color: rgb(128, 128, 128);">&gt;</span></div></div>
        </div>
        <span class="main-accentheader-title">
            Vue Instance
        </span>
        <span>
            Vue instance it global instance Vue library. It contains lot helpful methods and objects.
        </span>
        <div>
            Inside components, you can use <b>vueInstance</b> to get access to Vue instance.
        </div>
        <div>
            <div style="color: rgb(212, 212, 212); background-color: rgb(30, 30, 30); font-family: Consolas, &quot;Courier New&quot;, monospace; font-size: 14px; line-height: 19px; white-space: pre;"><div><span style="color: rgb(128, 128, 128);">&lt;</span><span style="color: rgb(86, 156, 214);">script</span><span style="color: rgb(128, 128, 128);">&gt;</span></div><div><span style="color: rgb(106, 153, 85);">//&nbsp;get&nbsp;ref&nbsp;from&nbsp;Vue&nbsp;instance</span></div><div><span style="color: rgb(86, 156, 214);">const</span>&nbsp;{&nbsp;<span style="color: rgb(79, 193, 255);">ref</span>&nbsp;}&nbsp;=&nbsp;<span style="color: rgb(156, 220, 254);">vueInstance</span>;</div><br><div><span style="color: rgb(197, 134, 192);">export</span>&nbsp;<span style="color: rgb(197, 134, 192);">default</span>&nbsp;{</div><div>&nbsp;&nbsp;&nbsp;&nbsp;<span style="color: rgb(156, 220, 254);">name:</span>&nbsp;<span style="color: rgb(206, 145, 120);">`TestComponent`</span>,</div><div>&nbsp;&nbsp;&nbsp;&nbsp;<span style="color: rgb(220, 220, 170);">setup</span>()&nbsp;{</div><div>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span style="color: rgb(106, 153, 85);">//using&nbsp;ref&nbsp;for&nbsp;setup&nbsp;component</span></div><div>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span style="color: rgb(86, 156, 214);">const</span>&nbsp;<span style="color: rgb(79, 193, 255);">repositories</span>&nbsp;=&nbsp;<span style="color: rgb(220, 220, 170);">ref</span>([]);</div><br><div>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span style="color: rgb(197, 134, 192);">return</span>&nbsp;{</div><div>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span style="color: rgb(156, 220, 254);">repositories</span></div><div>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;}</div><div>&nbsp;&nbsp;&nbsp;&nbsp;}</div><div>}</div><div><span style="color: rgb(128, 128, 128);">&lt;/</span><span style="color: rgb(86, 156, 214);">script</span><span style="color: rgb(128, 128, 128);">&gt;</span></div></div>
        </div>
    </div>
</template>

<script>
export default async function () {
    return {
        name: `Vue3Features`
    }
}
</script>

<style>
.vue3features-container {
    display: flex;
    flex-direction: column;
}
</style>