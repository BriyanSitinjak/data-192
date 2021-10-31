<template>
    <div class="auth-wrapper auth-v1">
        <div class="auth-inner">
            <v-card class="auth-card"> 
                <!-- logo -->
                <v-card-title class="d-flex align-center justify-center py-7">
                    <router-link
                    to="/"
                    class="d-flex align-center"
                    >
                        <v-img
                        :src="require('@/assets/logo.svg')"
                        max-height="50px"
                        max-width="50px"
                        alt="logo"
                        contain
                        class="me-3"
                        ></v-img>

                        <h2 class="text-2xl font-weight-semibold">
                            192.11
                        </h2>
                    </router-link>
                </v-card-title>

                <!-- title -->
                <v-card-text>
                    <p class="text-2xl font-weight-semibold text--primary mb-2">
                        Welcome to Our Platform
                    </p>
                    <p class="mb-2">
                        Please sign-in to your account and start the advanture
                    </p>
                </v-card-text>

                <!-- login form -->
                <v-card-text>
                    <v-form>
                        <v-text-field
                        v-model="email"
                        outlined
                        label="Email"                        
                        placeholder="dummy@example.com"
                        class="mb-3"
                        hide-details
                        ></v-text-field>

                        <v-text-field
                        v-model="password"
                        outlined
                        :type="isPasswordVisible ? 'text' : 'password'"
                        label="Password"
                        placeholder="............."
                        :append-icon="isPasswordVisible ? icons.mdiEyeOffOutline : icons.mdiEyeOutline"
                        @click:append="isPasswordVisible = !isPasswordVisible"
                        ></v-text-field>

                    </v-form>
                </v-card-text>
            </v-card>
        </div>
    </div>
</template>

<script>
import {mdiEyeOutline, mdiEyeOffOutline} from '@mdi/js'

export default {
    
}
</script>

<style lang="scss">
@import '~@/plugins/vuetify/default-preset/preset/pages/auth.scss';
</style>