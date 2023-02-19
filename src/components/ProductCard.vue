<!-- Product cards, bootstrap -->
<template>
    <div class="col">
        <div class="card" style="width: 18rem;">
            <img :src="prod.picture" class="card-img-top" alt="coffee">
            <div class="card-body">
                <p class="card-text"><strong>{{ prod.name }}</strong></p>
                <p class="card-text"> {{ prod.price }}kr</p>
            </div>
        </div>
</div>
</template>

<script>
export default {
    props: {
        prod: {
            required: true,
            type: Object
        }
    }
}
</script>
<style>
.col {
    display: flex;
    justify-content: center;
    margin-top: 2rem;
}
</style>
