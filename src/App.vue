<style>
form {
  display: flex;
  flex-direction: column;
}
form span {
  width: 80px;
  display: inline-block;
}
form input,
form select {
  width: 240px;
}
hr {
  border: 0;
  height: 1px;
  background-color: #eee;
  margin: 32px 0;
}
textarea {
  width: 560px;
  min-height: 240px;
}
</style>

<template>
  <div id="app">
    <form>
      <label>
        <span>Title</span>
        <input type="text" v-model="title" />
      </label>
      <label>
        <span>Name</span>
        <input type="text" v-model="name" />
      </label>
      <label>
        <span>Mobile</span>
        <input type="text" v-model="mobile" />
      </label>
    </form>
    <hr />
    <div v-html="html"></div>
    <hr />
    <textarea v-text="html"></textarea>
  </div>
</template>

<script>
export default {
  data: () => ({
    title: "Designer",
    name: "Panda WANG",
    mobile: "+86 175-2109-6154"
  }),
  computed: {
    html: function() {
      return `<div style="font-family:Verdana,sans-serif;font-size:x-small;color:#333;"><div>${this.title}&nbsp;·&nbsp;<b>${this.name}</b></div><div>Mobile&nbsp;·&nbsp;<b>${this.mobile}</b></div><img src="https://static.imcochina.com/signature.png" style="width:260px;height:60px;"><div>Website&nbsp;·&nbsp;<a href="https://www.imcochina.com"><b style="color:#0000ff">IMCOCHINA.COM</b></a></div></div>`;
    }
  }
};
</script>
