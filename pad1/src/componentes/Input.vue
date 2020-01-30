<template>
  <div>
    <div class="search-box">
      <div class="icon-search">
        <img src="img/icon-busca.svg" width="100%" />
      </div>
      <input v-model="inputName" type="text" placeholder="digite sua busca" class="input-search" />
    </div>
</template>

<script>
export default {
  data() {
    return {
      inputName: "",
      searched: false,
      listTattooers: [
        {
          id: 1,
          name: "Yohane Braga",
          instagram: "http://www.yohane.com.br",
          city: "Rio de Janeiro"
        },
        {
          id: 2,
          name: "Brian Gomes",
          instagram: "http://www.instagram.com/briangomes/",
          city: "São Paulo"
        },
        {
          id: 4,
          name: "Chiquinho Gomes",
          instagram: "https://www.instagram.com/chiquinhogtattoo",
          city: "São Paulo"
        }
      ],

      computed: {
        listTattooersFiltered() {
          if (this.searched) {
            let filtered = this.listTattooers.filter(tattooer => {
              return tattooer.name
                .toLowerCase()
                .includes(this.inputName.toLowerCase());
            });
            filtered = filtered.sort((a, b) => {
              return a.name.charAt() == b.name.charAt()
                ? 0
                : a.name.charAt() > b.name.charAt()
                ? 1
                : -1;
            });
            return filtered;
          }
          return [];
        }
      },
      methods: {
        search() {
          this.searched = true;
        }
      },
      watch: {
        inputName() {
          this.searched = false;
        }
      }
    };
  }
};
</script>

<style>
</style>