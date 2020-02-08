<template>
<div>
    <detail-banner></detail-banner>
</div>
</template>

<script>
    import DetailBanner from './components/banner'
    export default {
        name: 'Detail',
        components:{
            DetailBanner
        }

    }
</script>
<style lang='stylus' scoped>
    @import '~styles/varibles.styl';
    @import '~styles/mixins.styl';
</style>