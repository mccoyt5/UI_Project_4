<script>
    import { Link } from "svelte-routing";
</script>

<Link to="/">
    <button class="return">Go Back</button>
</Link>

<h2 id="patientName">Thomas McCoy</h2>

<svg width="400" height="500">
    <circle cx="70" cy="67" r="12.5" fill="black"/>
    <rect x="67.5" y="77" height="80" width="5"/>
    <circle cx="70" cy="167" r="10" fill="none" stroke="black" stroke-width="5"/>
    <rect x="67.5" y="177" height="80" width="5"/>
    <circle cx="70" cy="267" r="10" fill="none" stroke="black" stroke-width="5"/>
    <rect x="67.5" y="277" height="80" width="5"/>
    <circle cx="70" cy="367" r="10" fill="none" stroke="black" stroke-width="5"/>
    <rect x="67.5" y="377" height="80" width="5"/>
    <circle cx="70" cy="467" r="12.5" fill="black"/>
</svg>

<h2 id="checkin" class="timeline">12/7/2024: Admittance</h2>
<h2 id="app1" class="timeline">12/8/2024: Checkup</h2>
<h2 id="app2" class="timeline">12/9/2024: Surgery</h2>
<h2 id="app3" class="timeline">12/10/2024: Checkup</h2>
<h2 id="checkout" class="timeline">12/11/2024: Discharge</h2>

<style>
    .return {
        float: left;
        margin-top: 15px;
        margin-left: 20px;
    }

    #patientName {
        float: right;
        margin-top: 12.5px;
        margin-right: 20px;
        font-family:'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
        font-size: x-large;
    }

    .timeline {
        position: absolute;
        left: 725px;
        font-size: larger;
    }

    #checkin {
        top: 99px;
    }

    #app1 {
        top: 199px;
    }

    #app2 {
        top: 299px;
    }

    #app3 {
        top: 399px;
    }

    #checkout {
        top: 499px;
    }
</style>