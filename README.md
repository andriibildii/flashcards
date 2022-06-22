# Flashcards
In this project, I have practiced using ***Redux*** and ***Redux Toolkit*** to manage the complex state of a flashcard-style quiz app.

In the App, users able to create their own topics, quizzes for those topics, and flashcards for those quizzes.

Users will also be able to interact with their quizzes by flipping flashcards over.

------------
## Steps: 
1. In the `src/features/topics` directory, created a new file - `TopicsSlice.js`
   - with createdSlice() created `topicsSlice` (with name, initialState, reducer, action and selector)
2. Hooked the new topic form up to the action creator. In `src/components/NewTopicForm.js`
3. In the `src/features/quizzes` directory, created a new file - `QuizzesSlice.js`
    - with createdSlice() created `quizzesSlice` (with name, initialState, reducer, action and selector)
4. Added an action to the topics slice that adds a quiz’s id to the quizIds array of the topic with which the newly quiz is associated.
5. Wrote an action creator that returns a thunk that dispatches two actions one after the other. This new thunk action creator is the one that will dispatch when a user creates a new quiz.
6. Connected action creator to `src/components/NewQuizForm`
7. Imported the thunk action creator from quiz slice and dispatch it from the `handleSubmit()` event handler that fires when the new quiz form is submitted.
8. imported selector in `src/features/quizzes/Quizzes.js` and `src/features/quizzes/Quiz.js`
9. In the `src/features/cards` directory, created a new file - `CardsSlice.js`
- with `createdSlice()` created `cardsSlice` (with name, initialState, reducer, action and selector)
10. Connected addCard action creator to the new quiz form. In src/components/NewQuizForm, in the event handler that fires when the quiz form is submitted, iterated through the cards in that form’s local state.
11. The `Quiz` component renders a list of Card components, so in `src/features/cards/Card.js`, imported cards selector and used it to access all the cards in state.
12. Completed the `store.js` file

------------
## To Run

Run `npm start` in the project root and the app will be available on port 3000.

## Routes

- `/new-topic` – form to create a new topic
- `/topics` – index of all topics
- `/topics/:topicId` – page for an individual topic
- `/new-quiz` – form to create a new quiz
- `/quizzes` – index of all quizzes
- `/quizzes/:quizId` – page for an individual quiz

