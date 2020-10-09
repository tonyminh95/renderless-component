<template>
    <renderless-tags-input>
        <div slot-scope="{}" class="tags-input">
        <span class="tags-input-tag">
            <span>Testing</span>
            <span>Design</span>
            <button type="button" class="tags-input-remove">&times;</button>
        </span>
        <input class="tags-input-text" placeholder="Add tag...">
        </div>
    </renderless-tags-input>
</template>

<script>
    import RenderlessTagsInput from './components/RenderlessTagsInput'

    export default {
        components: { RenderlessTagsInput },

        data() {
            return {
                tags: ['Testing', 'Design']
            }
        }
    }
</script>
