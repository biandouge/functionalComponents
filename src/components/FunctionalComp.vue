<template functional>
<h1>FunctionalComp: {{ props.count}}</h1>
</template>
<script>
export default {
    functional: true,
    props: {
        count: Number,
    },
};
</script>
<style></style>