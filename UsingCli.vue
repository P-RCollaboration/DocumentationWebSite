<template>
    <div class="usingcli-container">
        <span class="main-header-title">
            Using CLI
        </span>
        <span class="main-subheader-title">
            ProvueCLI is console application help you in development and deployment application.
        </span>
        <span class="main-accentheader-title">
            Installation
        </span>
        <span>
            You can download the latest version for your OS at <a href="https://github.com/P-RCollaboration/ProvueCLI/releases">this link</a>.
        </span>
        <span class="main-accentheader-title">
            Setup project
        </span>
        <span>
            First of all you need setup folders - source folder, build folder and release folder.<br />
            You can do it via command-line argument or <b>provue</b> file.
            It will be useful place <b>provue</b> file to root of project directory.
            Example settings in <b>provue</b> file:
        </span>
        <div class="code-section">
            {<br />
                &quot;sourceFolder&quot;: &quot;src&quot;,<br />
                &quot;buildFolder&quot;: &quot;build&quot;,<br />
                &quot;releaseFolder&quot;: &quot;release&quot;<br />
            }
        </div>
        <span class="main-accentheader-title">
            Build for development
        </span>     
        <span>
            If you prepare <b>provue</b> file you just need run ProvueCLI in it without arguments.
            If you want use console argument you need specify it along with ProvueCLI.
        </span>
        <span>
            After you runned console application output can be something like:
        </span>
        <div class="code-section">
            <span>File is processing examples/helloworld App.vue...</span>
            <span>File is processing examples/helloworld ButtonsDemo.vue...</span>
            <span>File is processing examples/helloworld CheckBoxDemo.vue...</span>
        </div>
        <span class="main-accentheader-title">
            Build for release
        </span>     
        <span>
            While run ProvueCLI you need add argument <b>buildrelease</b> after it in release folder (releaseFolder parameter in provue file or same name argument from command line) placed release version.
            In release version components will be minification and uglifying (optionally).
        </span>
        <span class="main-accentheader-title">
            Run development server
        </span>     
        <span>
            ProvueCLI can runned as static webserver. You can specify <b>serverfolder</b> is folder that will be mapped in webserver and <b>host</b> and <b>port</b>. Default is localhost:8080.
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
.usingcli-container {
    display: flex;
    flex-direction: column;
}
</style>