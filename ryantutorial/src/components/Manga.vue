<template>
  <div class="container">
    <div class="row gap-2">
        <div class="card" v-for="data in jsonData" style="width: 18rem;" :key="data.id">
            <h5 class="card-title">{{data.name}}</h5>
            <p class="card-text">Genre:{{data.genre}}</p>
        </div>
    </div>
    <div id="list">
        <!-- <li v-for="mangas in Manga" :key="mangas.id"></li> -->
    </div>
  </div>
</template>

<script>
export default{
    data() {
        return {
            jsonData: []
        }
    },
    methods: {
        async jsData() {
          const response = await fetch(
            "https://masood-b.github.io/jsonServer/server.json"
          );
          //const jsonData = await response.json();
          let manga = await response.json()
            this.jsonData = manga.Manga;
        //  let info = jsonData.Manga;
        
         
        //   console.log(info);
        
        //   const result = document.querySelector("#list");
        
        //   info.forEach(data => {
        //     result.innerHTML =+`
        //     <div class="card" style="width: 18rem;">
        //             <img src="https://google.com" class="card-img-top" alt="...">
        //             <div class="card-body">
        //               <h5 class="card-title">${data.name}</h5>
        //               <p class="card-text">Genre:${data.genre}</p>
        //               <a href="#" class="btn btn-primary">Go somewhere</a>
        //             </div>
        //           </div>
        //     `;
        //   });
        }

    },
    created() {

    },
    mounted() {
        this.jsData()
    }
}

</script>

<style scoped></style>
