<template>
    <div class="carousel">
            <img v-show="activeImage==0" :src="images[3].big">
            <transition name = "fade">
                <img v-show="activeImage==0" :src="images[activeImage].big">
            </transition>
            <img v-show="activeImage==1" :src="images[0].big">
            <transition name = "fade">
                <img v-show="activeImage==1" :src="images[activeImage].big">
            </transition>
            <img v-show="activeImage==2" :src="images[1].big">
            <transition name = "fade">
                <img v-show="activeImage==2" :src="images[activeImage].big">
            </transition>
            <img v-show="activeImage==3" :src="images[2].big">
            <transition name = "fade">
                <img v-show="activeImage==3" :src="images[activeImage].big">
            </transition>
        <div v-on:click="nextImg" class="carousel-nav-next">
            <a class="icon is-small">
                <font-awesome-icon :icon="['fas', 'chevron-right']"/>
            </a>
        </div>
        <div v-on:click="nextImg" class="carousel-nav-prev">
            <a class="icon is-small">
                <font-awesome-icon :icon="['fas', 'chevron-left']"/>
            </a>
        </div>

        <div class="main-logo-wrapper">
            <img class="main-logo" src="/logo-white.png">
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
.fade-enter-active, .fade-leave-active {
    transition: 0.5s ease-out;
}

.fade-enter, .fade-leave-to {
    opacity: 0;
}
a {
    color:white;
}
a:hover {
    color:#cecece;
}
</style>