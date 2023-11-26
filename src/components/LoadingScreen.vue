<template>
    <div v-if="!allImagesLoaded" id="overlay" class="d-flex justify-center align-center">
        <div class="loader">
            <div className="loader__outline"></div>
            <img src="../assets/895.png" alt="Loading" className="loader__image" />
        </div>
    </div>
</template>
<script>
export default {
    name: "LoadingScreen",
    data() {
        return {
            imageUrls: [
                'bp.jpg',
                'ts.jpg',
                'zoukOut.jpg',
                'Home.jpg',
                'upcomingEvents.jpg',
                'pastEvents.jpg',
                'ndp.jpg',
                'taeyeon.jpg'
            ],
            loadedImages: 0, 
        };
    },
    computed: {
        allImagesLoaded() {
            return this.loadedImages === this.imageUrls.length;
        },
    },
    mounted() {
        this.imageUrls.forEach((url) => {
            const img = new Image();
                img.onload = this.imageLoaded;
                img.src = this.getImageUrl(url);
        });
    },
    methods: {
        imageLoaded() {
            this.loadedImages += 1;
        },
        getImageUrl(name, ext) {
            return new URL(`../assets/${name}`, import.meta.url).href
        }
    },
    watch: {
        allImagesLoaded: function() {
            if(this.allImagesLoaded){
                document.documentElement.style.overflowY = 'auto';
                document.body.style.overflowY = 'auto';
                return;
            }

            document.documentElement.style.overflowY = 'hidden';
            document.body.style.overflowY = 'hidden';
        }
    }
}
</script>
<style>
#overlay {
    height: 100vh;
    width: 100vw;
    background-image: linear-gradient(to right, #2F2482 , #E0037C);
}

.loader {
  position: relative;
  width: 150px;
  height: 150px;
  animation: spin 1.5s linear infinite;
  border: 4px solid #f3f3f3; /* Outline color */
  border-top: 4px solid #3498db; /* Spinner color */
  border-radius: 50%;
}

.loader__outline {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  border-radius: 50%;
  border: 4px solid #f3f3f3; /* Outline color */
}

.loader__image {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  width: calc(100% - 8px); /* Take up the inner circle with a small padding */
  height: calc(100% - 8px);
  border-radius: 50%;
  object-fit: cover;
}

@keyframes spin {
  0% { transform: rotate(0deg); }
  100% { transform: rotate(360deg); }
}
</style>