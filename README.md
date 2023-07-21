// Пример кода на JavaScript: Простой TODO-лист

const todos = [];

function addTodo(todo) {
  todos.push(todo);
}

function removeTodo(index) {
  if (index >= 0 && index < todos.length) {
    todos.splice(index, 1);
  }
}

function displayTodos() {
  console.log("Список TODO:");
  todos.forEach((todo, index) => {
    console.log(`${index + 1}. ${todo}`);
  });
}

if (typeof module !== 'undefined' && module.exports) {
  // Для возможности использования кода в Node.js
  module.exports = {
    addTodo,
    removeTodo,
    displayTodos
  };
}
