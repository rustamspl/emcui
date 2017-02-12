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
        pass: '',
        doLogin () {
          console.log(data.login);
        }
     };
    export default {
    data(){ return data }
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
