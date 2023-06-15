<script>
    // Importing Link
    import {Link} from 'svelte-routing'
    import {courses, courseId} from '../stores.js'    
</script>
<main class="home-container">
    {#each $courses as course }
        <div class="course-card">
            <img class="img" src="img/image{course.id+1}.jpg" alt="">
            <h3 class="name">{course.name}</h3>

            <!-- Feedback Button -->
            <Link to="feedbackpage">
                <button class="button" on:click={courseId.set(course.id)}>Feedback</button>
            </Link>
        </div>
    {/each}
</main>
