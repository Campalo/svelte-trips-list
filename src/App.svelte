<script>
  import Trip from "./Trip.svelte";

  let destination = "";
  let duration = "";
  let date = "";
  let participants = "";
  let details = "";

  //   function SetDestination(event) {
  //     destination = event.target.value;
  //   }
</script>

<style>
  h1 {
    color: rgb(44, 43, 43);
    text-align: center;
  }
  /* form style starts */
  form {
    display: flex;
    flex-direction: column;
    margin: 40px 80px;
  }
  div {
    display: flex;
    flex-direction: row;
    align-items: baseline;
    width: 100%;
  }
  label {
    width: 30%;
  }
  input,
  textarea {
    width: 70%;
  }
  .btn__container {
    display: flex;
    justify-content: center;
  }
  .btn__style {
    text-align: center;
    background-color: rgb(240, 178, 23);
    width: 200px;
    height: 40px;
    margin: 20px;
  }
  /* form style ends */
</style>

<h1>Plan your next trips</h1>
<form>
  <div>
    <!-- bind:value : when the value is updated in the input it will update the var value asap and keep the format-->
    <label for="destination">Destination:</label>
    <input
      type="text"
      id="destination"
      value={destination}
      bind:value={destination} />
  </div>

  <div>
    <label for="duration">Duration (in days):</label>
    <input type="number" id="duration" value={duration} bind:value={duration} />
  </div>

  <div>
    <label for="date">Date:</label>
    <input type="date" id="date" value={date} bind:value={date} />
  </div>

  <div>
    <label for="participants">Participants names:</label>
    <input
      type="text"
      id="participants"
      value={participants}
      bind:value={participants} />
  </div>

  <div>
    <label for="details">Details:</label>
    <textarea id="details" value={details} biend:value={details} />
  </div>

  <div class="btn__container">
    <input class="btn__style" type="submit" value="Add your trip" />
  </div>
</form>

<Trip
  TripDestination={destination}
  TripDuration={duration}
  TripDate={date}
  TripParticipants={participants}
  TripDetails={details} />
