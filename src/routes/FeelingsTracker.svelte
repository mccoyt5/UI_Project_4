<script>
    import { Link } from "svelte-routing";

    let entries = []

    function recordMessage() {
        // @ts-ignore
        document.getElementById("journal").value = "Here is an example of someone speaking and it populating the text field.";
    }

    // This function stores the journal entry and pain scale rating
    // This would be used to display the information in the family member/loved one side of the application
    // Since this is only the patient side of the application, the data isn't used
    function submitEntry() {
        // @ts-ignore
        if(document.getElementById("1").checked){
            // @ts-ignore
            entries.push([document.getElementById("journal").value, document.getElementById("1").value]);
        }
        // @ts-ignore
        if(document.getElementById("2").checked){
            // @ts-ignore
            entries.push([document.getElementById("journal").value, document.getElementById("2").value]);
        }
        // @ts-ignore
        if(document.getElementById("3").checked){
            // @ts-ignore
            entries.push([document.getElementById("journal").value, document.getElementById("3").value]);
        }
        // @ts-ignore
        if(document.getElementById("4").checked){
            // @ts-ignore
            entries.push([document.getElementById("journal").value, document.getElementById("4").value]);
        }
        // @ts-ignore
        if(document.getElementById("5").checked){
            // @ts-ignore
            entries.push([document.getElementById("journal").value, document.getElementById("5").value]);
        }
        alert("Entry saved!"); 
    }
</script>

<Link to="/">
    <button class="return">Go Back</button>
</Link>

<h2 id="patientName">Thomas McCoy</h2>

<br/>
<p id="journalLabel"> Write about how you're feeling today.</p>
<textarea id="journal"></textarea>
<button on:click={recordMessage}>Record Message</button>

<br/>
<br/>
<p>Rate how much pain you feel on a scale of 1-5.</p>
<p>1 is the lowest and 5 is the highest.</p>
<br/>
<form>
    <label>1
        &nbsp
        <input type="radio" name="pain" id = "1" value="1" checked/>
    </label>
    &nbsp
    &nbsp
    &nbsp
    <label>2
        &nbsp
        <input type="radio" name="pain" id = "2" value="2"/>
    </label>
    &nbsp
    &nbsp
    &nbsp
    <label>3
        &nbsp
        <input type="radio" name="pain" id = "3" value="3"/>
    </label>
    &nbsp
    &nbsp
    &nbsp
    <label>4
        &nbsp
        <input type="radio" name="pain" id = "4" value="4"/>
    </label>
    &nbsp
    &nbsp
    &nbsp
    <label>5
        &nbsp
        <input type="radio" name="pain" id = "5" value="5"/>
    </label>
</form>

<br/>

<button id="submit" on:click={submitEntry}>Submit Entry</button>

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

    #journalLabel {
        float: left;
        margin-top: 20px;
        margin-left: 50px;
    }

    #journal {
        height: 275px;
        width: 355px;
        resize: none;
    }

    input {
        transform: scale(2);
    }

    #submit {
        height: 40px;
        width: 200px;
    }
</style>