<template>
    <div class="button-components-container">
        <span class="main-header-title">
            ButtonState
        </span>
        <span class="main-subheader-title">
            The button is often rectangle block that can be pressed and after it, something happens.
        </span>
        <span class="main-accentheader-title">
            Props
        </span>
        <span>
            <b>title</b> <i>(string)</i> this property hold text for the button. It is often placed inside the button rectangle.
        </span>
        <span>
            <b>disable</b> <i>(boolean)</i> this property hold flag if the button is disabled it means that the button not active.
        </span>
        <span class="main-accentheader-title">
            Methods
        </span>
        <span>
            <b>click(Event)</b> <i>(void)</i> the method needs a call after the button is pressed.
        </span>
        <span class="main-accentheader-title">
            Emits
        </span>
        <span>
            <b>clicked(Event)</b> called after method <b>click</b> was called and <b>disable</b> property is false.
        </span>
    </div>
</template>

<script>
export default {
    name: `Button`
}
</script>

<style>
.button-components-container {
    display: flex;
    flex-direction: column;
}
</style>