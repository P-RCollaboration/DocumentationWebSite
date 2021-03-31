<template>
    <div class="menu-container">
        <div v-for="(group, index) in groups" :key="index">
            <div
                class="group-container"
                @click="group.opened = !group.opened">
                <span>{{ group.title }}</span>
                <font-icon-state
                    group="fas"
                    :id="group.opened ? `fa-chevron-up` : `fa-chevron-down`"
                    size="16px">
                    <template #default="{ context }">
                        <font-icon-view :context="context"></font-icon-view>
                    </template>
                </font-icon-state>
            </div>
            <div
                class="option-container"
                v-show="group.opened">
                <div
                    v-for="(option, optionIndex) in group.options"
                    :key="optionIndex"
                    @click="selectItem(option)">
                    <span
                        :class="{ 'selected-item': selectedItem === option }">
                        {{ option.title }}
                    </span>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: `AppMenu`,
    data() {
        return {
            selectedItem: null,
            groups: [
                {
                    title: `Getting started`,
                    opened: false,
                    options: [
                        {
                            title: `Introduction`,
                            link: `/introduction`
                        },
                        {
                            title: `Install`,
                            link: `/install`
                        },
                        {
                            title: `Using CLI`,
                            link: `/usingcli`
                        },
                        {
                            title: `Loading components`,
                            link: `/loadingcomponents`
                        }                            
                    ]
                },
                {
                    title: `Components`,
                    opened: false,
                    options: [
                        {
                            title: `Button`
                        },
                        {
                            title: `RadioButton`
                        },
                        {
                            title: `FontIcon`
                        },
                        {
                            title: `DropDown`
                        },
                        {
                            title: `CheckBox`
                        },
                        {
                            title: `CheckBoxTriState`
                        },
                        {
                            title: `TextBox`
                        },
                        {
                            title: `NumberBox`
                        },
                        {
                            title: `TextArea`
                        },
                        {
                            title: `Slider`
                        },
                    ]
                },
                {
                    title: `Layouts`,
                    opened: false,
                    options: [
                        {
                            title: `ListBox`
                        }
                    ]
                },
                {
                    title: `Validation`,
                    opened: false,
                    options: [
                        {
                            title: `Introduction`
                        },
                        {
                            title: `ValidateHost`
                        }
                    ]
                }
            ]
        }
    },
    mounted() {
        let path = location.hash.replace(`#`, ``);
        if (path === `/`) path = `/introduction`;
        
        const option = this.groups.reduce((left, right) => left.concat(right.options), []).find(a => a.link === path);
        if (!option) return;
        
        const group = this.groups.find(group => group.options.find(option => option === option));
        if (!group) return;
        
        this.selectedItem = option;
        group.opened = true;
    },
    methods: {
        selectItem(option) {
            this.selectedItem = option;
            this.$router.push({ path: option.link });
        }
    }
}
</script>

<style>
.group-container {
    display: flex;
    flex-direction: row;
    align-items: center;
    user-select: none;
}
.group-container > span {
    margin-right: 8px;
    font-weight: 600;
    justify-self: stretch;
    font-size: 1rem;
    flex: 1;
}
.menu-container {
    margin-top: 10px;
    margin-right: 40px;
    width: 140px;
}
.selected-item {
    font-weight: bold;
}
.option-container {
    padding-left: 4px;
    font-size: 0.9rem;
    user-select: none;
}
</style>

