<template>
    <div class="contact-form-wrapper">
        <form
                @submit="checkForm"
                action="/submission"
                method="post"
                novalidate="true"
                            >
                <div class="field">
                    <label class="label">NÉV *</label>
                    <div class="control">
                        <input v-model="name" class="input" type="text" name="Name">
                    </div>
                </div>

                <div class="field">
                    <label class="label">E-MAIL CÍM *</label>
                    <div class="control">
                        <input v-model="email" class="input" type="text" name="Email">
                    </div>
                </div>

            <div class="field">
                <label class="label">MILYEN TÍPUSÚ FOTÓZÁS ÉRDEKELNE? *</label>
                
                <div class="control"> 
                    <label class="radio">
                    <input v-model="service" type="radio" name="service" value="Jegyes">
                    Jegyes
                    </label>
                    <label class="radio">
                    <input v-model="service" type="radio" name="service" value="Esküvő">
                    Esküvői
                    </label>
                    <label class="radio">
                    <input v-model="service" type="radio" name="service" vlaue="Család">
                    Család
                    </label>
                </div>
            </div>

            <div class="field">
                <label class="label">HONNAN HALLOTTÁL RÓLUNK?</label>
                <div class="control">
                    <div class="select is-primary">
                        <select name="Source">
                            <option></option>
                            <option>Facebook</option>
                            <option>Instagram</option>
                            <option>Google</option>
                            <option>Ismerős</option>
                            <option>Egyéb</option>
                        </select>
                    </div>
                </div>
            </div>
            
            <div class="field">
                <label class="label">ÜZENETED SZÁMUNKRA *</label>
                <div class="control">
                    <textarea v-model="message" class="textarea" name="Message"></textarea>
                </div>
            </div>

            <div v-if="errors.length>0" v-for="error in errors" class="is-fullhd">
                <div class="notification">
                    {{error}}
                </div>
            </div>

            

            <button id="send-valid-form" class="is-hidden" type="submit"></button>


            <div class="control has-text-centered">
                <button class="button is-primary" @click="sendForm">Küldés</button>
            </div>


        </form>
    </div>
</template>

<script>
export default {
    data() {
        return {
            name: null,
            email: null,
            message: null,
            service: '',
            errors: []
        }
    },
    methods: {
        sendForm () {
            document.getElementById("send-valid-form").click(); // Click on the checkbox
        },
        onSubmit () {
        const axiosConfig = {
            header: { "Content-Type": "application/x-www-form-urlencoded" }
        };
        this.$axios.post(
            "/",
            this.encode({
            ...this.form
            }),
            axiosConfig
            ).then(() => {
                this.$router.push("/submission");
            })
            .catch((e) => {
                console.log(e)
                this.$router.push("/404");
            });
        },
        checkForm:function(e) {

            if (this.name && this.email && this.message && this.service) {
                return true;
            }

            this.errors = [];

            if (!this.name) {
                console.log(this.name)
                this.errors.push('A név megadása kötelező.');
            }
            if (!this.email) {
                console.log(this.email)
                this.errors.push('Az email megadása kötelező.');
            }
            if (!this.service) {
                console.log(this.service)
                this.errors.push('Kérlek jelöld meg melyik szolgáltatás iránt érdeklődsz.');
            }
            if (!this.message) {
                console.log(this.message)
                this.errors.push('Üzenet kitöltése kötelező');
            }

            e.preventDefault();
      
        },
        encode (data) {
            return Object.keys(data)
                .map(
                key => `${encodeURIComponent(key)}=${encodeURIComponent(data[key])}`
                )
                .join("&");
        },
        
    }
}
</script>

<style lang="scss">
.contact-form-wrapper {
    background-color: #fff;
    padding: 60px;
}
</style>