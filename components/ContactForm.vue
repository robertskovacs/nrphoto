<template>
    <div class="contact-form-wrapper">
        <form name="contact" method="POST" data-netlify="true">
            <div class="field">
                <label class="label">NÉV *</label>
                <div :bind="name" class="control">
                    <input class="input" type="text" name="Name">
                </div>
            </div>

            <div class="field">
                <label class="label">E-MAIL CÍM *</label>
                <div class="control">
                    <input :bind="type" class="input" type="text" name="Email">
                </div>
            </div>

            <div class="field">
                <label class="label">MILYEN TÍPUSÚ FOTÓZÁS ÉRDEKELNE? *</label>
                <div class="control">
                    <label class="radio">
                    <input type="radio" name="service">
                    Jegyes
                    </label>
                    <br>
                    <label class="radio">
                    <input type="radio" name="service">
                    Esküvői
                    </label>
                    <br>
                    <label class="radio">
                    <input type="radio" name="service">
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
                    <textarea :bind="message" class="textarea" name="Message"></textarea>
                </div>
            </div>

            <div v-if="errors.length>0" v-for="error in errors" class="is-fullhd">
                <div class="notification">
                    {{error}}
                </div>
            </div>

            
            <div class="control has-text-centered">
                <button class="button is-primary" @click="checkForm" type="submit">Küldés</button>
            </div> 
        </form>
    </div>
</template>

<script>
export default {
    data() {
        return {
            name: "",
            email: "",
            message: "",
            type:"",
            errors: ""
        }
    },
    methods: {
        validation () {
            if(!this.name || !this.email || !this.message) {
                this.error="A csillaggal jelölt mezők kitöltése kötelező."
            }
        },
        
        checkForm (e) {
            if (this.name && this.email && this.message) {
                router.push("/submission")
                return true;
            }

            this.errors = [];

            if (!this.name) {
                this.errors.push('A név megadása kötelező.');
            }
            if (!this.email) {
                this.errors.push('Az email megadása kötelező.');
            }
            if (!this.type) {
                this.errors.push('Kérlek jelöld meg melyik szolgáltatás iránt érdeklődsz.');
            }
            if (!this.message) {
                this.errors.push('Üzenet kitöltése kötelező');
            }

            e.preventDefault();

      
        }
    }
}
</script>

<style lang="scss">
.contact-form-wrapper {
    background-color: #fff;
    padding: 60px;
}
</style>