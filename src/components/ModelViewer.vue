<script>
    import * as THREE from "three";
    import { GLTFLoader } from 'three/addons/loaders/GLTFLoader.js';
    import { OrbitControls } from "three/examples/jsm/controls/OrbitControls.js";

    export default {
        name: "ModelViewer",

        mounted() {
            this.initModel();
        },

        methods: {
            initModel() {
                const scene = new THREE.Scene();

                const ambientLight = new THREE.AmbientLight(0xffffff, 1);
                scene.add(ambientLight);

                const directionalLight = new THREE.DirectionalLight(0xffffff, 1);
                scene.add(directionalLight);

                const camera = new THREE.PerspectiveCamera(
                    75,
                    window.innerWidth/1.5 / window.innerHeight/1.5,
                    0.1,
                    1000
                );

                const renderer = new THREE.WebGLRenderer( { alpha: true } );
                
                renderer.setSize(window.innerWidth/1.5, window.innerHeight/1.5);
                
                renderer.setClearColor( 0x000000, 0 ); // set background color
                this.$refs.modelContainer.appendChild(renderer.domElement);

                const loader = new GLTFLoader();
                
                loader.load("/src/assets/Dea.gltf", (gltf) => {
                    const dogModel = gltf.scene;

                    dogModel.position.set(0, -0.5, 0);

                    scene.add(dogModel);

                    camera.position.y = 1;
                    camera.position.z = 1.75;

                    const controls = new OrbitControls(camera, renderer.domElement);

                    const animate = function () {
                        requestAnimationFrame(animate);

                        dogModel.rotation.y -= 0.005;

                        controls.update();

                        renderer.render(scene, camera);
                    };

                    animate();

                    function onWindowResize() {
                        const newWidth = window.innerWidth/1.5;
                        const newHeight = window.innerHeight/1.5;

                        camera.aspect = newWidth / newHeight;
                        camera.updateProjectionMatrix();

                        renderer.setSize(newWidth, newHeight);
                    }

                    window.addEventListener('resize', onWindowResize);
                    onWindowResize();

                });
            },
        },
    };
</script>

<template>
    <div ref="modelContainer" class="container"></div>
</template>

<style scoped>
    .container {
        width: 100%;
        height: auto;

        display: flex;
        justify-content: center;
        align-items: center;
    }
</style>  