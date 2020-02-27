<script>

import { Link } from 'yrv';

export let link;
export let text;
export let page;
export let align = "center";

let selected = link === page;

let selectedStyle = selected ? "font-black cursor-default" : "hover:font-extrabold";

</script>

<div
    class="w-40 m-5 text-gray-400 text-{align} { selectedStyle }">
    { #if selected } 
        [ { text } ]
    { :else }
        <Link href="#{ link }">{ text }</Link>
    { /if }
</div>