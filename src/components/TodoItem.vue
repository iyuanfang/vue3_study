<template>
<li>{{msg}}</li>
</template>

<script>
export default {
    name: 'TodoItem',
    props: {
        msg: String
    }
}
</script>
