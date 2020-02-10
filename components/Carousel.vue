<template>
    <div class="carousel">
        <img :src="images[activeImage].big">
        <div class="carousel-nav-next">
            <button class="button" v-on:click="nextImg">next</button>
        </div>
        <div class="carousel-nav-prev">
            <button class="button" v-on:click="prevImg">prev</button>
        </div>
        
    </div>
</template>

<script>
export default {
    data() {
        return {
            //Array to hold all carousel images
            images: [
                {
                    id: '1',
                    big: 'images/p1.jpeg',
                    thumb: 'images/thumbs/p1.jpeg'
                },
                {
                    id: '2',
                    big: 'images/p2.jpeg',
                    thumb: 'images/thumbs/p2.jpeg'
                },
                {
                    id: '3',
                    big: 'images/p3.jpeg',
                    thumb: 'images/thumbs/p3.jpeg'
                },
                {
                    id: '4',
                    big: 'images/p4.jpeg',
                    thumb: 'images/thumbs/p4.jpeg'
                }
            ],
            //Index of the active image on the images array
            activeImage: 0
        }
    },
    mounted () {
        this.timer()
    },
    methods: {
        nextImg () {
            if(this.activeImage < this.images.length-1) {
                this.activeImage += 1
            } else {
                this.activeImage = 0
            }
        },
        prevImg () {
            if(this.activeImage > 0) {
                this.activeImage -= 1
            } else {
                this.activeImage = this.images.length - 1
            }
            
        },
        timer () {
            let _this = this
            setInterval(function(){
                _this.nextImg();
                }, 8000);
        }
    }
}
</script>
<style lang="scss" scoped>
img {
    width: 100%;
    height:100%;
}
</style>