const defDiv = document.getElementById('definition');
const guessInput = document.getElementById('guess');
const submitBtn = document.getElementById('submitGuess');
const resultDiv = document.getElementById('result');

let currentWord = "";

async function fetchRandomWord() {
  try {
    const resp = await fetch('https://random-word-api.vercel.app/api?words=1');
    const data = await resp.json();
    return Array.isArray(data) ? data[0] : null;
  } catch {
    return null;
  }
}

async function fetchDefinition(word) {
  try {
    const resp = await fetch(`https://api.dictionaryapi.dev/api/v2/entries/en/${word}`);
    const data = await resp.json();
    if (Array.isArray(data) && data[0]?.meanings?.length) {
      return data[0].meanings[0].definitions[0].definition;
    }
    return null;
  } catch {
    return null;
  }
}

async function loadWord() {
  defDiv.textContent = "Loading...";
  currentWord = await fetchRandomWord();
  let definition = null;

  if (currentWord) {
    definition = await fetchDefinition(currentWord);
  }

  if (!currentWord || !definition) {
    currentWord = "error";
    defDiv.textContent = "something went wrong fetching the word.";
  } else {
    defDiv.textContent = definition;
  }

  resultDiv.textContent = "";
  guessInput.value = "";
}

submitBtn.addEventListener("click", () => {
  const guess = guessInput.value.trim().toLowerCase();
  if (!currentWord || currentWord === "error") {
    resultDiv.textContent = "⚠️ Can't play this round (error).";
    return;
  }

  if (guess === currentWord.toLowerCase()) {
    resultDiv.textContent = "✅ Correct!";
  } else {
    resultDiv.textContent = `❌ Wrong! The word was: ${currentWord}`;
  }

  setTimeout(loadWord, 3000);
});

loadWord();
