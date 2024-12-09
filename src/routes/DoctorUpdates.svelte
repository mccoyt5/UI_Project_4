<script>
    import { Link } from "svelte-routing";
</script>

<Link to="/">
    <button class="return">Go Back</button>
</Link>

<h2 id="patientName">Thomas McCoy</h2>

<table>
    <thead>
        <tr>
            <th>Date</th>
            <th>Doctor</th>
            <th>Update</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>
            12/7/2024
            </td>
            <td>
            Dr. Andre
            </td>
            <td>
            Fever
            </td>
        </tr>
        <tr>
            <td>
            12/8/2024
            </td>
            <td>
            Dr. Jones
            </td>
            <td>
            Lower fever, slight cough
            </td>
        </tr>
        <tr>
            <td>
            12/8/2024
            </td>
            <td>
            Dr. Jones
            </td>
            <td>
            No changes
            </td>
        </tr>
        <tr>
            <td>
            12/9/2024
            </td>
            <td>
            Dr. Andre
            </td>
            <td>
            Fever gone, severe cough
            </td>
        </tr>
        <tr>
            <td>
            12/9/2024
            </td>
            <td>
            Dr. Jones
            </td>
            <td>
            No changes
            </td>
        </tr>
    </tbody>
</table>

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

    table {
        height: 90%;
        width: 90%;
        margin: auto;
        border-collapse: collapse;
        color: #000000;
        background-color: #93a4c49c;
        border: 1px solid #3a3a4f;
    }

    th {
        border: solid;
    }

    tr {
        border: solid;
    }

    td {
        border: solid;
    }
</style>