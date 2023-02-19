<template>
    <div>
        <p>{{ content }}</p>
        <div class="c">
            <QuillEditor v-model:content="content" content-type="html" output="html"/>

        </div>
</div>  </template>

<script>
import { QuillEditor } from '@vueup/vue-quill'
import BlotFormatter from 'quill-blot-formatter'
import '@vueup/vue-quill/dist/vue-quill.snow.css'

export default {

    setup: () => {
        const modules = {
            name: 'blotFormatter',
            module: BlotFormatter,
            options: {/* options */ }
        }
        return { modules }
    },
    components: {
        QuillEditor
    },
    data() {
        return {
            options: {
                debug: 'info',
                modules: {
                    toolbar: ['bold', 'italic', 'underline']
                },
                placeholder: '...',
                readOnly: false,
                theme: 'snow',
                // return: 'html'
            },

            content: '',
        }
    }
}
</script>

<style></style>