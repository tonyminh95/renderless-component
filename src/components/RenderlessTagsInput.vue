<script>
    export default {
        name: 'RenderlessTagsInput',

        props: ['value'],

        render() {
            return this.$scopedSlots.default({
                tags: this.value
            })
        }
    }
</script>
