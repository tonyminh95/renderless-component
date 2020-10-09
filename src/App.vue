<template>
    <renderless-tags-input v-model='tags'>
        <div slot-scope='{ tags, removeTag, inputAttrs, inputEvents }' class='tags-input'>
            <span class='tags-input-tag'>
                <span v-for='(tag, index) in tags' :key='index'>
                    {{ tag }}

                    <button type='button' class='tags-input-remove'
                        @click='removeTag(tag)'
                    >
                        &times;
                    </button>
                </span>
            </span>

            <input class="tags-input-text" placeholder="Add tag..."
                v-bind="inputAttrs"
                v-on="inputEvents"
            >
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
