<template>
    <div id="consulting">
        <h5>FUSIONS & AQUISITIONS</h5>
        <h1>Insurance</h1>
        <h1>Consulting</h1>
        <div class="input_first_row">
          <input type="text" placeholder="Name" />
          <input type="email" placeholder="Email" />
        </div>
        <div>
          <input type="number" placeholder="Phone" />
          <select name="info" id="info">
            <option value="">More info</option>
            <option value="Option1">Option1</option>
            <option value="Option2">Option2</option>
            <option value="Option3">Option3</option>
          </select>
        </div>
        <button class="btn btn_green">GET IN TOUCH</button>
        <button class="btn btn_white">READ MORE</button>
    </div>
</template>

<script>
export default {
    name: 'MyJumbotronCard'
}
</script>

<style scoped lang="scss">
@import '../style/vars.scss';

#consulting {
      position: absolute;
      right: 15%;
      bottom: 30%;

      h5 {
        color: $c5;
      }

      h1 {
        font-size: 4rem;
        font-weight: bold;
      }

      input,
      select {
        margin-right: 10px;
        margin-bottom: 10px;
        padding: 10px;
        background-color: $c6;
        border: 1px solid $c6;
        border-radius: 4px;
      }

      .input_first_row {
        margin-top: 20px;
      }

      select {
        color: grey;
        width: 47%;
      }

      .btn_white{
        margin-left: 15px;
        background-color: #e1e5e6;
        color: $c2;
      }
    }
</style>