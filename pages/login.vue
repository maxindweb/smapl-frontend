<template>
    <div>
        <v-container>
            <v-row justify-lg="center" align="end">
                <v-col cols="6">
                    <v-card>
                        <v-form>
                            <template>
                                <v-container>
                                    <v-text-field
                                    v-model="email"
                                    label="email"
                                    ></v-text-field>
                                    <v-text-field
                                    v-model="password"
                                    label="password"
                                    ></v-text-field>
                                </v-container>
                            </template>
                            <v-row>
                                <v-col>
                                    <v-btn
                                    type="submit"
                                    color="info"
                                    > Login</v-btn>
                                </v-col>
                            </v-row>
                        </v-form>
                    </v-card>
                </v-col>
            </v-row>
        </v-container>
    </div>
</template>
<script>
export default {
    data: () => ({
      drawer: null,
      loading: false,
      email: undefined,
      password: undefined,
      
}),
    methods: {
        async login(){
            var res = $axios.post('/auth/login')
        }
    },
}
</script>