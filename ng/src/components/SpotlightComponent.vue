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
                { title: 'Custom keyboards', desc: 'Multiple keyboard styles', img: 'src/assets/keyboard.png', buttonTxt: 'Get your set' }
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
    div {
        width: 80vw;
        margin: 80px auto;
        display: flex;
    }

    @media (max-width: 1100px) {
        div#spotlightContainer {
            flex-direction: column;
        }
    }
</style>