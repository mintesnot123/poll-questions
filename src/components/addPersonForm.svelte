<script>
    let firstName = "";
    let lastName = "";
    let age;
    let skills = [];
    let profesion;
    const handleSubmit = () => {
        console.log(
            firstName,
            " ",
            lastName,
            " ",
            age,
            " ",
            skills,
            " ",
            profesion
        );
    };
</script>

<form on:submit|preventDefault={handleSubmit}>
    <p>Add New Person</p>
    <input type="text" placeholder="First Name" bind:value={firstName} />
    <input type="text" placeholder="Last Name" bind:value={lastName} />
    <input type="number" placeholder="Age" bind:value={age} /><br />
    <input type="checkbox" bind:group={skills} value="fighting" />fighting<br />
    <input type="checkbox" bind:group={skills} value="sneaking" />sneaking<br />
    <input type="checkbox" bind:group={skills} value="running" />running<br />
    <select name="" id="" bind:value={profesion}>
        <option value="front-end">Front-end developer</option>
        <option value="back-end">Back-end developer</option>
        <option value="full-stack">Full-stack developer</option>
    </select>
    <button type="submit">Add</button>
</form>

<style>
</style>
