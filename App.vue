<template>
    <div class="app-container">
        <app-menu>

        </app-menu>
        <div class="content-container">
            
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
}
</style>