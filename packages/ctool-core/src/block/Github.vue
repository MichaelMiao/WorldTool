<script setup lang="ts">
import {onMounted} from "vue"
import axios from "axios";
import storage from "@/helper/storage";
import {openUrl} from "@/helper/helper"

const CACHE_NAME = 'github_star';

let star = $ref(storage.get<number>(CACHE_NAME) || 0)

onMounted(() => {
})

</script>

<style scoped>
.ctool-github span {
    cursor: pointer;
    display: inline-flex;
    align-items: center;
    column-gap: 5px;
    font-size: 12px;
    height: 24px;
    padding: 2px 5px;
    text-decoration: none;
}

.ctool-github span:hover {
    color: var(--ctool-primary-hover);
}

.ctool-github .ctool-github-name {
    border: 1px solid var(--form-element-border-color);
    border-radius: 3px 0 0 3px;
}

.ctool-github .ctool-github-star {
    border: 1px solid var(--form-element-border-color);
    border-left: none;
    font-weight: bold;
    border-radius: 0 3px 3px 0;
}
</style>
