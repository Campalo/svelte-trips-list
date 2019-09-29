<script>
  // make the variables available in the parent
  export let TripDestination;
  export let TripDuration;
  export let TripDate;
  export let TripParticipants;
  export let TripDetails;
</script>

<style>
  section {
    padding: 1rem;
    margin: 0.5rem;
    background-color: aliceblue;
    border-radius: 8px;
    box-shadow: 2px 2px 5px 0px rgba(0, 0, 0, 0.4);
    color: dimgrey;
  }
</style>

<section>
  <h2>Destination: {TripDestination}</h2>
  <h3>Duration: {TripDuration} days</h3>
  <h3>Date: {TripDate}</h3>
  <h4>Participants: {TripParticipants}</h4>
  <p>Details: {TripDetails}</p>
</section>
