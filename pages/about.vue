<template>
  <div> 
    <h1><About<i>{{name}}</i></h1>
    <h2>age <b>{{age}}</b></h2>
    sex <b>{{sex}}</b>
    <h1 v-if ="OK"</h1>
    <h2 v-show="OK"></h2>
    <input :value="name.substr(3,2)" type="text"><br>
    <input v-model="name" type="text"><br>
    <input v-model="age" type="text"><br>
    <input v-model="sex" type="text"><br>
    <input type='button' @click="doSave" value='save'>
  </div>
</template>
<script>
export default {
  data() {
    return {
      name: "supreeya",
      age: 25,
      sex: "หญิง",
      OK: true,
      members: [{ id: 1, name: "name1", org }]
    };
  },
  computed: {
    upperName() {
      return this.name.toUpperCase();
    },

    newName() {
      var tmp = this.name.split("");
      if (tem.length === 1) {
        return this.name;
      }

      return tem[0] + "" + tmp[1].substr(1, 3);
    }
  },
  methods: {
    doSave() {
      this.name = this.name + "*";
      this.OK = !this.OK;
    },
    doSave2() {
      this.name - this.newName;
      this.doSave();
    }
  }
};
</script>

