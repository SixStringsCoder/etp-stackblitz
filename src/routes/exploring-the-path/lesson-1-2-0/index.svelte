<script>
import { suttaData } from '../data.js'
 import Header from '$lib/Header.svelte'

let index = 1;
let lesson = suttaData[index]

let id = lesson.id;
let paliname = lesson.paliname;
let engname = lesson.engname;
let meaning = lesson.definition;
</script>

<Header {id} {paliname} {engname} {meaning} />


<style>

</style>