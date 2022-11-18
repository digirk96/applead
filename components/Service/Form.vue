<template>
<div class="right-bottom">
    <h2>Meet with Us</h2>
    <form class="form" @submit.prevent="submitform">

        <div class="form-wrapper">
            <div class="form-group">
                <label for="name">Name</label>
                <input type="text" name="name" placeholder="Name" v-model="contact.name">
                <span style="color:rgba(255, 0, 0, 0.473); font-size:1.4rem"></span>

            </div>
            <div class="form-group">
                <label for="phone">Phone</label>
                <input type="text" name="phone" placeholder="Phone" v-model="contact.phone">
                <span style="color:rgba(255, 0, 0, 0.473); font-size:1.4rem"></span>
            </div>
            <div class="form-group">
                <label for="email">Your Email</label>
                <input type="text" name="email" placeholder="Email id" v-model="contact.email">
                <span style="color:rgba(255, 0, 0, 0.473); font-size:1.4rem"></span>
            </div>

            <div class="form-group">
                <label for="message">Message</label>
                <textarea name="message" cols="25" rows="4" placeholder="Text" v-model="contact.message"></textarea>
                <span style="color:rgba(255, 0, 0, 0.473); font-size:1.4rem"></span>
            </div>
        </div>
        <button type="submit" class="submit-btn">Submit</button>
    </form>
</div>
</template>

<script setup>

const router = useRouter()
let contact = {
    name: '',
    email: '',
    phone: '',
    message: ''
};



function submitform() {

    const response = useFetch('https://appleadtechnologies.com/applead/api/contact', {
        method: 'post',
        body: contact
    })

    router.push('/thank-you');

    
}


</script>

<style scoped>
.right-bottom {
    width: 100%;
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    justify-content: flex-start;
}

.right-bottom h2 {
    font-size: 1.8rem;
    color: #000;
    margin-bottom: 1.5rem;
}

.form {
    width: 100%;
    border-radius: 1rem;
    display: flex;
    align-items: center;
    justify-content: center;
    flex-direction: column;
    gap: 1.5rem;
    padding: 2rem 1.5rem;
    box-shadow: rgba(50, 50, 93, 0.25) 0px 2px 5px -1px,
        rgba(0, 0, 0, 0.3) 0px 1px 3px -1px;
}

.form-wrapper {
    width: 100%;
    display: flex;
    flex-direction: column;
    gap: 1.5rem;
}

.form-group {
    display: flex;
    flex-direction: column;
    gap: 1rem;
}

input {
    padding: 1rem;
    background-color: #ececec;
    border-radius: 3px;
    font-size: 1.4rem;
    color: #000;;
    font-weight: 500;
    width: 100%;
    outline: none;
    border: none;
}

textarea {
    padding: 1rem;
    width: 100%;
    background-color: #ececec;
    border: none;
    border-radius: 3px;
    font-size: 1.4rem;
    color: #000;
    font-weight: 500;
    outline: none;
}

.submit-btn {
    width: 100%;
    font-size: 1.4rem;
    color: #fff;
    background-color: #527abc;
    border: none;
    padding: 1rem 0;
    border-radius: 3px;
}
</style>
