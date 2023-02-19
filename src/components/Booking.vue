<!-- Boknings komponent, formulär -->
<template>
    <form class="form row g-3 needs-validation" novalidate>
        <div class="col-md-4">
            <label for="validationCustom01" class="form-label">Förnamn</label>
            <input type="text" class="form-control" id="validationCustom01" v-model="first" required>
        </div>
        <div class="col-md-4">
            <label for="validationCustom02" class="form-label">Efternamn</label>
            <input type="text" class="form-control" id="validationCustom02" v-model="last" required>
        </div>
        <div class="col-md-3">
            <label for="validationCustom04" class="form-label">Tid</label>
            <select class="form-select" id="validationCustom04" v-model="time" required>
                <option selected disabled value="">Välj tid</option>
                <option>10:00</option>
                <option>10:30</option>
                <option>11:00</option>
                <option>11:30</option>
                <option>12:00</option>
                <option>12:30</option>
                <option>13:00</option>
                <option>13:30</option>
                <option>14:00</option>
                <option>14:30</option>
                <option>15:00</option>
                <option>15:30</option>
            </select>
        </div>
        <div class="col-12">
            <button class="btn btn-secondary" type="submit" @click="submit">Boka</button>
        </div>
</form>
</template>

<script>
export default {
    data() {
        return {
            first: '',
            last: '',
            time: ''
        }
    },
    methods: {
        submit() {
            alert("Tack för din beställning " + this.first + ", vi ses klockan " + this.time + " imorgon")
        }
    }

}
</script>

<style>
.form {
    position: absolute;
    top: 90%;
    left: 50%;
    transform: translate(-50%, -50%);
    background-color: rgba(255, 255, 255, 0.7);
    padding: 2rem;
}
</style>
