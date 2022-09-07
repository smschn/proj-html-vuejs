<template>
    <div class="employee_card d_flex">
        <img v-bind:src="employeeProps.imgSrc" v-bind:alt="employeeProps.name">
        <div class="employee_info">
            <h4>{{employeeProps.name}}</h4>
            <h6>{{employeeProps.role}}</h6>
            <i class="fa-brands fa-facebook-f icon-background"></i>
            <i class="fa-brands fa-twitter"></i>
            <i class="fa-brands fa-linkedin-in"></i>
        </div>
    </div>
</template>

<script>
export default {
    name: 'MySection4Card',
    props: {
        employeeProps: Object
    }
}
</script>

<style scoped lang="scss">
@import '../style/vars.scss';

.employee_card {
    margin-top: 30px;
    flex-basis: calc(100% / 2 - 10px);

    img {
        width: 80px;
        border-radius: 5px;
    }

    .employee_info {
        padding: 4px 0 4px 20px;

        h6 {
            margin: 15px 0;
            color: $c1;
        }

        i:before {
            margin: 0 5px;
            width: 20px;
            height: 20px;
            border-radius: 50%;
            text-align: center;
            line-height: 20px;
            vertical-align: middle;
            padding: 5px;
            background-color: $c12;
            display: inline-block;
            color: $c5;
        }
    }
}
</style>