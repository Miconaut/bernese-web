<script>
    import { reactive, watch } from 'vue';
    import PhotoSwipeLightbox from 'photoswipe/lightbox';
    import 'photoswipe/style.css';

    export default {
        name: 'Gallery',

        data() {
            return {
                lightbox: null,
            };
        },

        props: {
            galleryID: String,
            images: Array,
        },

        setup(props) {
            // Reactive ref for images
            const loadedImages = reactive({
                value: [],
            });

            // Trigger a reactivity update when the images prop changes
            watch(() => props.images, () => {
                loadedImages.value = props.images;
            });

            return {
                loadedImages,
            };
        },

        mounted() {
            if (!this.lightbox) {
                this.lightbox = new PhotoSwipeLightbox({
                    gallery: '#' + this.$props.galleryID,
                    children: 'a',
                    pswpModule: () => import('photoswipe'),
                });
                this.lightbox.init();
            }
        },
        
        unmounted() {
            if (this.lightbox) {
                this.lightbox.destroy();
                this.lightbox = null;
            }
        },

        methods: {},
    };
</script>

<template>
    <div :id="galleryID">
        <a v-for="(image, key) in images" :key="key"
        :href="image.url" :data-pswp-width="image.width" :data-pswp-height="image.height"
        target="_blank" rel="noreferrer" >
            <img :src="image.url" alt="" />
        </a>
  </div>
</template>

<style scoped>
    img {
        width: 20rem;
        height: 15rem;

        object-fit: cover;
    }
</style>