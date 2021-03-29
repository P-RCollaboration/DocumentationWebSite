<template>
    <div>
        <div>
            <span>Documentation for version 1.0</span>
        </div>
        <div class="app-container">
            <app-menu>
            </app-menu>
            <div class="content-container">
                <router-view></router-view>
            </div>
        </div>
    </div>
</template>

<script>
export default async function () {
    require.resolveStyles(`https://cdn.jsdelivr.net/npm/bootstrap@5.0.0-beta2/dist/css/bootstrap.min.css`);
    require.resolveStyles(`https://use.fontawesome.com/releases/v5.0.13/css/all.css`);
    await globalComponent(`https://p-rcollaboration.github.io/CoreComponents/src/states/FontIconState.vue`);
    await globalComponent(`https://p-rcollaboration.github.io/CoreComponents/src/views/fontawesome/FontIconView.vue`);
    const AppMenu = await remoteComponent(`AppMenu.vue`);

    return {
        name: `App`,
        data() {
            return {
            }
        },
        methods: {
        },
        components: {
            AppMenu
        }
    }
}
</script>

<style>
.app-container {
    display: flex;
    flex-direction: row;
    justify-content: center;
}
.content-container {
    width: 800px;
    padding-left: 30px;
}
.main-header-title {
    font-weight: bold;
    font-size: 1.8rem;   
}
.main-subheader-title {
    font-size: 1.3rem;
}
.main-accentheader-title {
    margin-top: 10px;
    font-weight: bold;
    font-size: 1.5rem;
}
</style>