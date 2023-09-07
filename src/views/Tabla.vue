<template>
    <v-card
      class="mx-auto"
      max-width="1000"
    >
        <v-table 
            density="compact"
        >
        <thead>
            <tr>
            <th class="text-left">
                Autor
            </th>
            <th class="text-left">
                Título
            </th>
            <th class="text-left">
                Post
            </th>
            </tr>
        </thead>
        <tbody>
            <tr
            v-for="autor in datos1"
            :key="autor.id"
            >
                <td>{{ autor.name }}</td>
                <tr
                v-for="post in datos2"
                :key="post.userId"
                >
                <td>{{ post.title }}</td>
                <td>{{ post.body }}</td>
                </tr>
            </tr>
        </tbody>
        </v-table>
    </v-card>
  </template>

  <script>
    export default{
        data1(){
            return{
                datos1: [],
            };
        },
        async created(){
            let urlAutor="https://jsonplaceholder.typicode.com/users";
            let urlPost="https://jsonplaceholder.typicode.com/posts";
            const response1 = await fetch(urlAutor);
            const autorData = await response1.json();
            this.datos1=autorData;
            const response2 = await fetch(urlPost);
            const postData = await response2.json();
            this.datos2 = postData;
        },
        data2(){
            return{
                datos2:[],
            };
        },
     };
  </script>