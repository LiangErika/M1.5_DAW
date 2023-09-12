<template>
    <VNavigationDrawer
        expand-on-hover
        rail
    >

        <v-divider></v-divider>

        <v-list density="compact" nav>
          <v-list-item prepend-icon="mdi-view-dashboard" title="Home" value="home" @click="dirigirHome"> </v-list-item>
          <v-list-item prepend-icon="mdi-domain" title="Table" value="table" @click="dirigirTabla"></v-list-item>
        </v-list>
        
    </VNavigationDrawer>
</template>

<script>
    export default{
        methods:{
            dirigirHome(){
                this.$router.push('/');
            },
            dirigirTabla(){
                this.$router.push('/crud');
            }
        }
    }
    
</script>

