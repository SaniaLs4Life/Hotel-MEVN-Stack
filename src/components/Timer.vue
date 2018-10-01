<template>
        <kbd>{{ days }} days : {{ hours }} h : {{ minutes }} m : {{ seconds }} s</kbd>
</template>

<script>
export default {
    name: 'Timer',
    props: {
        date: {
            type: String
        }
    },
    data() {
        return {
            now: 0,
            count: 0
        }
    },
    methods: {
        timer_loop() {
            this.count++
            this.now = Math.trunc(new Date().getTime() / 1000)
            this.count < 200 && setTimeout(this.timer_loop, 1000)
        }
    },
    mounted() {
        this.timer_loop()
    },
    computed: {
        seconds() {
            return (this.modifiedDate - this.now) % 60
        },
        minutes() {
            return Math.trunc((this.modifiedDate - this.now) / 60 ) % 60
        },
        hours() {
            return Math.trunc((this.modifiedDate - this.now) / 60 / 60) % 24
        },
        days() {
            return Math.trunc((this.modifiedDate - this.now) / 60 / 60 / 24)
        },
        modifiedDate() {
            return Math.trunc(Date.parse(this.date) / 1000)
        }
    }
}
</script>

<style>

</style>
