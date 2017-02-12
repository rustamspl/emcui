<template>
    <div class="login">
        <h3>
            Вход
        </h3>
        <form  @submit.prevent="doLogin">
            <div class="row">
                <input placeholder="Логин" type="text" v-model="login" name="login" />
            </div>
            <div class="row">
                <input placeholder="Пароль" type="password" v-model="pass"/>
            </div>
            <div class="control">
                <button type="submit">
                    Вход
                </button>
            </div>
        </form>
    </div>
</template>
<script>
    var data={
        login: 'aaa',
        pass: ''
     };
    export default {
    data(){ return data }
    ,methods:{
        doLogin () {
          console.log(data.login);
        }
    }
}
</script>
<style scoped="">
.login{
  width: 200px;
  height: 300px;
  margin: auto auto;
}
.row,.control{
  padding: 5px;
}
.control{

}
input{
  width:150px;
  margin: 0;

}
</style>
