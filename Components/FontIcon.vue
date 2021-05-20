<template>
    <div class="fonticon-components-container">
        <span class="main-header-title">
            FontIconState
        </span>
        <span class="main-subheader-title">
            Icons based on web font it industrial standart. You can use 
        </span>
        <span class="main-accentheader-title">
            Props
        </span>
        <span>
            <b>id</b> <i>(string)</i> is the icon identifier (in fontawesome fa-address-card as example).
        </span>
        <span>
            <b>group</b> <i>(string)</i> is the icon a group (if appropriate).
        </span>
        <span>
            <b>size</b> <i>(string)</i> size of icon as CSS. default `16px`.
        </span>
    </div>
</template>

<script>
export default {
    name: `FontIcon`
}
</script>

<style>
.fonticon-components-container {
    display: flex;
    flex-direction: column;
}
</style>