<template>
    <div id="spotlightContainer">
        <SpotlightItemComponent v-for="(item, index) in SpotlightItems" :key="index" :item="item" />
    </div>
</template>

<script>
import SpotlightItemComponent from '../components/SpotlightItemComponent.vue'

export default {
    components: {
        SpotlightItemComponent
    },
    data() {
        return {
            SpotlightItems: [
                { title: 'Authentic mousepads', desc: 'Up to 50 different designs', img: 'src/assets/mousepad.png', buttonTxt: 'Get your pad' },
                { title: 'Custom keyboards', desc: 'Multiple keyboard styles', img: 'src/assets/keyboard.png', buttonTxt: 'Get your board' }
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
    div#spotlightContainer {
        width: 80vw;
        margin: 100px auto 70px auto;
        display: flex;
        justify-content: space-between;
        align-items: center;
        gap: 50px;
    }

    @media (max-width: 1100px) {
        div#spotlightContainer {
            flex-direction: column;
        }
    }
</style>