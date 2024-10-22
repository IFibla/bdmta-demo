<script lang="ts">
    import Textfield from '@smui/textfield';
    import SegmentedButton, { Segment, Label } from '@smui/segmented-button';
    let choices = ['Low', 'Medium', 'High'];
    let valueA = "jasd";
</script>

<svelte:head>
	<title>Strategy Simulator</title>
</svelte:head>

<div id="central-slot">
    <h2>Strategy Simulator</h2>
    <h6>Big Data Management, Technologies and Analytics</h6>

    <div id="input-bar">
        <Textfield bind:value={valueA} label="Number of laps" />
        <Textfield bind:value={valueA} label="Target lap time" />
        <Textfield bind:value={valueA} label="Average pit stop loss" />
    </div>

    <SegmentedButton segments={choices} let:segment singleSelect>
        <Segment {segment}>
        <Label>{segment}</Label>
        </Segment>
    </SegmentedButton>

</div>

<style>
    #central-slot {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
        row-gap: 10px;
	}

    #input-bar {
        display: flex;
        flex-direction: row;
        justify-content: center;
        align-items: center;
        column-gap: 10px;
        width: 100%;
    }
</style>