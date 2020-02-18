<template>
    <div class="tile is-ancestor">
        <div class="tile is-vertical">
            <div class="tile">

            <div class="tile is-parent is-vertical">
                <article class="tile is-child">
                    <figure class="image is-3by5">
                        <img src="https://images.pexels.com/photos/3700513/pexels-photo-3700513.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=750&w=1260">
                    </figure>
                </article>
                <article class="tile is-child">
                    <figure class="image is-4by3">
                        <img src="https://images.pexels.com/photos/3661353/pexels-photo-3661353.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=750&w=1260">
                    </figure>
                </article>
            </div>
            
            <div class="tile is-parent is-vertical">
                <article class="tile is-child">
                <figure class="image is-4by3">
                    <img src="https://images.pexels.com/photos/3373366/pexels-photo-3373366.jpeg?auto=compress&cs=tinysrgb&dpr=1&w=500">
                </figure>
                </article>
                <article class="tile is-child">
                <figure class="image is-4by5">
                    <img src="https://images.pexels.com/photos/3645370/pexels-photo-3645370.jpeg?auto=compress&cs=tinysrgb&dpr=1&w=500">
                </figure>
                </article>
                <article class="tile is-child">
                <figure class="image is-4by3">
                    <img src="https://images.pexels.com/photos/3046404/pexels-photo-3046404.jpeg?auto=compress&cs=tinysrgb&dpr=1&w=500">
                </figure>
                </article>
                <article class="tile is-child">
                <figure class="image is-4by3">
                    <img src="https://images.pexels.com/photos/3614358/pexels-photo-3614358.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=750&w=1260">
                </figure>
                </article>
            </div>

            <div class="tile is-parent is-vertical">
                <article class="tile is-child">
                <figure class="image is-4by3">
                    <img src="https://images.pexels.com/photos/3294248/pexels-photo-3294248.jpeg?auto=compress&cs=tinysrgb&dpr=1&w=500">
                </figure>
                </article>
                <article class="tile is-child">
                <figure class="image is-4by5">
                    <img src="https://images.pexels.com/photos/3617467/pexels-photo-3617467.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=750&w=1260">
                </figure>
                </article>
                <article class="tile is-child">
                <figure class="image is-4by3">
                    <img src="https://images.pexels.com/photos/3596695/pexels-photo-3596695.jpeg?auto=compress&cs=tinysrgb&dpr=1&w=500">
                </figure>
                </article>
            </div>

            </div>
        </div>
    </div>
</template>

<script>
export default {
    data () {
        return {
            first: 2,
            images: [
                "https://bulma.io/images/placeholders/640x480.png",
                "https://bulma.io/images/placeholders/640x480.png",
                "https://bulma.io/images/placeholders/640x480.png",
                "https://bulma.io/images/placeholders/640x480.png",
                "https://bulma.io/images/placeholders/640x480.png",
                "https://bulma.io/images/placeholders/640x480.png",
                "https://bulma.io/images/placeholders/640x480.png",
                "https://bulma.io/images/placeholders/640x480.png",
                "https://bulma.io/images/placeholders/640x480.png",
                "https://bulma.io/images/placeholders/640x480.png",
            ]
        } 
    }
}
</script>
<style lang="scss" scoped>
img, figure {
    height: 100% !important;
}
</style>