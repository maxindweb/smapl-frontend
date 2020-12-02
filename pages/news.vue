<template>
    <v-container>
        <h1>News</h1>
    </v-container>
</template>
<script>
export default {
    data: () => ({
        post: []
    }),

    methods: {
        fetchAllPost(){
            return axios.get('http://127.0.0.1:8000/v1/post/published')
        },
        async getPost(){
            try{
                const res = await this.fetchAllPost()
                this.post = res.data
            }catch(err){
                console.log(err)
            }
        }
    },
}
</script>