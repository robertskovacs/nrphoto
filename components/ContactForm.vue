<template>
    <div class="contact-form-wrapper">
        <form
            netlify
            name="contact">   
                <div class="field">
                    <label class="label">NÉV *
                        <div class="control">
                            <input v-model="form.name" class="input" type="text" name="name">
                        </div>
                    </label>
                </div>


            <div class="field">
                <label class="label">E-MAIL CÍM *</label>
                <div class="control">
                    <input v-model="form.email" class="input" type="text" name="email">
                </div>
            </div>

            <div class="field">
                <label class="label">MILYEN TÍPUSÚ FOTÓZÁS ÉRDEKELNE? *</label>
                
                <div class="control"> 
                    <label class="radio">
                    <input v-model="form.service" type="radio" name="service" value="Jegyes" @click="ddTestVm.ddTestSelectedOption = option.value">
                    Jegyes
                    </label>
                    <label class="radio">
                    <input v-model="form.service" type="radio" name="service" value="Esküvő">
                    Esküvői
                    </label>
                    <label class="radio">
                    <input v-model="form.service" type="radio" name="service" value="Család">
                    Család
                    </label>
                </div>
            </div>

            <div class="field">
                <label class="label">HONNAN HALLOTTÁL RÓLUNK?</label>
                <div class="control">
                    <div class="select is-primary">
                        <select name="Source" v-model="form.source">
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
                    <textarea v-model="form.message" class="textarea" name="message"></textarea>
                </div>
            </div>

            <div v-if="errors.length>0" v-for="error in errors" class="is-fullhd">
                <div class="notification">
                    {{error}}
                </div>
            </div>

            <div class="control has-text-centered">
                <button class="button is-primary" type="submit" @click.prevent="checkForm">Küldés</button>
            </div>

        </form>
    </div>
</template>

<script>
import axios from 'axios';
export default {
    data() {
        return {
            form: {
                name: '',
                email: '',
                message: '',
                service: '',
                source: ''
            },
            errors: []
        }
    },
    methods: {
        encode (data) {
        return Object.keys(data)
            .map(
            key => `${encodeURIComponent(key)}=${encodeURIComponent(data[key])}`
            )
            .join("&");
        },
        handleSubmit() {
            fetch('/', {
                method: 'POST',
                headers: { 'Content-Type': 'application/x-www-form-urlencoded' },
                body: this.encode({ 'form-name': 'contact', ...this.form }),
            })
                .then(() => this.$router.push("/submission"))
                .catch(error =>
                this.$router.push("/404"));
        },
        checkForm (e) {
            if (this.form.name && this.form.email && this.form.message && this.form.service) {
                this.handleSubmit()
            }

            this.errors = [];

            if (!this.form.name) {
                console.log(this.form.name)
                this.errors.push('A név megadása kötelező.');
            }
            if (!this.form.email) {
                console.log(this.form.email)
                this.errors.push('Az email megadása kötelező.');
            }
            if (!this.form.service) {
                console.log(this.form.service)
                this.errors.push('Kérlek jelöld meg melyik szolgáltatás iránt érdeklődsz.');
            }
            if (!this.form.message) {
                console.log(this.form.message)
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