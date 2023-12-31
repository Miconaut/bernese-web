<script>
    import Header from './components/Header.vue'
    import ModelViewer from './components/ModelViewer.vue'
    import Texts from './components/Texts.vue'
    import Gallery from './components/Gallery.vue'

    export default {
        name: 'App',
        components: {
            Header,
            ModelViewer,
            Texts,
            Gallery,
        },

        data() {
            return {
                images: [],
            };
        },

        mounted() {
            const folderPath = 'src/assets/Dea';

            const imageExtension = 'jpg';

            const promises = [];

            // Simulate fetching images from a folder
            for (let i = 1; i <= 62; i++) {
                const imageUrl = `${folderPath}/img-${i}.${imageExtension}`;

                // Create a promise for each image
                const promise = new Promise((resolve) => {
                    const img = new Image();
                    img.src = imageUrl;

                    img.onload = () => {
                        console.log(`Image loaded: ${imageUrl}`);
                        console.log(`Natural dimensions: ${img.naturalWidth} x ${img.naturalHeight}`);

                        // Resolve the promise with image details
                        resolve({
                            url: imageUrl,
                            width: img.naturalWidth,
                            height: img.naturalHeight,
                        });
                    };
                });

                promises.push(promise);
            }

            // Wait for all promises to resolve
            Promise.all(promises).then((images) => {
                // Set the images data in component state
                this.images = images;
                console.log('Images:', this.images);
            });
        },
    };
</script>

<template>
    <div>
        <Header />
        <main>
            <ModelViewer />
            <Texts />
            <Gallery galleryID="gallery" :images="images" />
        </main>
    </div>
</template>

<style scoped>
    div {
      display: flex;
      flex-direction: column;
    }

    #gallery {
        display: flex;
        flex-direction: row;
        flex-wrap: wrap;
        justify-content: center;
        align-items: center;
        gap: 1rem;
    }
</style>
