import React, { useState } from 'react';

const SearchBar = ({ onSearch }) => {
  const [query, setQuery] = useState('');

  const handleSubmit = (e) => {
    e.preventDefault();
    onSearch(query);
  };

  return (
    <form className="flex items-center gap-2 mb-6" onSubmit={handleSubmit}>
      <input
        type="text"
        className="border rounded px-3 py-2 w-full focus:outline-none focus:ring-2 focus:ring-blue-300"
        placeholder="Search books, authors, or keywords..."
        value={query}
        onChange={e => setQuery(e.target.value)}
      />
      <button
        type="submit"
        className="bg-blue-600 text-white px-4 py-2 rounded hover:bg-blue-700 transition"
      >
        Search
      </button>
    </form>
  );
};

export default SearchBar;
