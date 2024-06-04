<script>
import { store } from '/src/components/data/store'



export default {
    components: {
        AppMain
    },
    data() {
        return {
            store

        }
    },
    methods: {
        getImage(nomefile) {
            return new URL(`../assets/${nomefile}, import.meta.url`);
            },
        },
        prevImage() {
            this.store.posts--
            if (this.store.posts < 0)
                this.store.posts = 2
            console.log(this.store.img[this.data.posts].badge);
        },
        nextImage() {
            this.store.posts++
            if (this.store.posts> 2)
                this.store.posts = 0
            console.log(this.store.posts[this.data.posts].badge);
        },
        visible(i) {
            if (i <= this.store.posts + 3 && i >= this.store.posts) {
                return true
            }
        },

        
        mounted() {
        console.log(this.store.posts)
        }
    }
    

</script>

<!-- this.store.cards[this.store.currentCards].path -->

