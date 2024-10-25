<template>
    <div ref="threeContainer" style="width: 100%; height: 100vh;"></div>
  </template>
  
  <script>
  import * as THREE from 'three';
  
  export default {
    name: 'RotatingSphere',
    mounted() {
      this.initThree();
      this.animate();
    },
    methods: {
      initThree() {
        // Scene, Camera, Renderer
        this.scene = new THREE.Scene();
        this.camera = new THREE.PerspectiveCamera(75, window.innerWidth / window.innerHeight, 0.1, 1000);
        this.renderer = new THREE.WebGLRenderer({ antialias: true });
        this.renderer.setSize(window.innerWidth, window.innerHeight);
        this.renderer.setPixelRatio(window.devicePixelRatio);
        this.$refs.threeContainer.appendChild(this.renderer.domElement);
  
        // Sphere Geometry
        const geometry = new THREE.SphereGeometry(1, 32, 32);
        const material = new THREE.MeshStandardMaterial({ color: 0x0077ff });
        this.sphere = new THREE.Mesh(geometry, material);
        this.scene.add(this.sphere);
  
        // Directional Light
        const directionalLight = new THREE.DirectionalLight(0xffffff, 1); // White light with full intensity
        directionalLight.position.set(5, 5, 5); // Positioning the light
        directionalLight.castShadow = true;     // Enable shadow casting if needed
        this.scene.add(directionalLight);
  
        // Optional: Helper to visualize the light direction
        const lightHelper = new THREE.DirectionalLightHelper(directionalLight, 1);
        this.scene.add(lightHelper);
  
        // Camera position
        this.camera.position.z = 5;
  
        // Resize Event Listener
        window.addEventListener('resize', this.onWindowResize);
      },
      animate() {
        requestAnimationFrame(this.animate);
  
        // Rotate Sphere
        this.sphere.rotation.y += 0.01;
        this.sphere.rotation.x += 0.01;
  
        // Render Scene
        this.renderer.render(this.scene, this.camera);
      },
      onWindowResize() {
        // Update camera aspect ratio and renderer size on window resize
        this.camera.aspect = window.innerWidth / window.innerHeight;
        this.camera.updateProjectionMatrix();
        this.renderer.setSize(window.innerWidth, window.innerHeight);
      },
    },
    beforeDestroy() {
      // Clean up event listener when component is destroyed
      window.removeEventListener('resize', this.onWindowResize);
    },
  };
  </script>
  
  <style scoped>
  /* Optional: add any additional styling here */
  </style>
  