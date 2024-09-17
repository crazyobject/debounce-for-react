# react-use-debounce

A simple react hook for debouncing an input with state variables in react.

## Installation

```bash
npm i debounce-for-react
```

## Usage

[Live demo](https://stackblitz.com/edit/react-debounce-hook)

```javascript
import React, { useState } from "react";
import { useDebounce } from "debounce-for-react";

function ExampleComponent() {
  const [value, setValue] = useState("");
  const debouncedValue = useDebounce(value, 500);

  useEffect(() => {
    // Use debouncedValue for API calls or other effects
  }, [debouncedValue]);

  return (
    <div>
      <input
        type="text"
        value={value}
        onChange={(e) => setValue(e.target.value)}
        placeholder="Type something..."
      />
      <p>Debounced Value: {debouncedValue}</p>
    </div>
  );
}
```
