<template>
    <div class="carousel">

        <img  v-if="show" :src="images[prevImage]">
        <transition name = "fade">
            <img v-if="show" :src="images[activeImage]">
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
        

        <figure class="main-logo-wrapper">
            <img class="main-logo" src="/logo-white.png">
        </figure>
        
    </div>
</template>

<script>
export default {
    data() {
        return {
            images: [
                    '/images/1.jpg',
                    '/images/2.jpg',
                    '/images/3.jpg',
                    '/images/4.jpg'
            ],
            activeImage: 0,
            prevImage: null,
            show: true
        }
    },
    mounted () {
        this.timer()
    },
    watch: {
        activeImage: function (newImg, oldImg) {
            this.show =! this.show
            let _this = this
                setTimeout(function(){
                    _this.show =! _this.show
                    }, 10);
            if(this.activeImage == 0) {
                this.prevImage = this.images.length - 1
            } else {
                this.prevImage = this.activeImage - 1
            }
        }
    },
    methods: {
        nextImg () {
            if(this.activeImage < this.images.length - 2) {
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
                }, 4500);
        }
    }
}
</script>
<style lang="scss" scoped>
.fade-enter-active, .fade-leave-active {
    transition: 0.8s ease-out;
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

.carousel-nav-next {
	position: relative;
    z-index: 1;
	color: white;
	float: right;
	top:50%;
	margin-right:3rem;
	font-size: 50px;
}

.carousel-nav-prev {
	position: relative;
    z-index: 1;
	color: white;
	float: left;
	top:50%;
	margin-left:3rem;
	font-size: 50px;
}
.main-logo-wrapper {
    position: relative;
    display:block;
    margin-left: auto;
    margin-right: auto;
    width:150px;
    height:150px;
	top:80%;
    
}

.main-logo-wrapper > img {
    width:100%;
    height:100%;
    z-index: 1;
    position: absolute;
}
</style>