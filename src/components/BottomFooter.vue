<template>
    <footer>
        <SponsorContainer />
        <SomeBox />
    </footer>
</template>

<script>
import SponsorContainer from './SponsorContainer.vue'
import SomeBox from './SomeBox.vue';

export default {
    name: 'BottomFooter',
    components: {
        SponsorContainer,
        SomeBox
    }
}
</script>

<style>
footer div.someBox a.some_icon{
    color: var(--lightBlue);
}
</style>