<template>
    <div class="radio-button-components-container">
        <span class="main-header-title">
            RadioButtonsState
        </span>
        <span class="main-subheader-title">
            Radio buttons are normally presented in radio groups (a collection of radio buttons describing a set of related options). Only one radio button in a group can be selected at the same time.
        </span>
        <span class="main-accentheader-title">
            Props
        </span>
        <span>
            <b>value/moduleValue</b> <i>(string, number, object)</i> this property hold text for the button. It is often placed inside the button rectangle.
        </span>
        <span>
            <b>group</b> <i>(string)</i> this property holds the group name for the underlying HTML component.
        </span>
        <span>
            <b>disable</b> <i>(string)</i> this property hold flag if the button is disabled it means that the button not active.
        </span>
        <span>
            <b>validators</b> <i>(object)</i> a set of rules for validating a component value.
        </span>
        <span>
            <b>validateHost</b> <i>(object)</i> a validation context is an object that defines a group of components to be validated together.
        </span>
        <span class="main-accentheader-title">
            Methods
        </span>
        <span>
            <b>setRadioState(value)</b> <i>(void)</i> the method needs for change radio value.
        </span>
        <span>
            <b>select(value)</b> <i>(void)</i> need call after was clicked on the radio the button in HTML component.
        </span>
        <span>
            <b>validate()</b> <i>(void)</i> perform validating on single component.
        </span>
        <span class="main-accentheader-title">
            Emits
        </span>
        <span>
            <b>changed(newValue)</b> called after method <b>select</b> was called and <b>disable</b> property is false.
        </span>
    </div>
</template>

<script>
export default {
    name: `RadioButton`
}
</script>

<style>
.radio-button-components-container {
    display: flex;
    flex-direction: column;
}
</style>