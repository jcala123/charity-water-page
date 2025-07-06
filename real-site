import React, { useState } from "react";
import confetti from "canvas-confetti";

const backgroundImageUrl =
  "https://media.licdn.com/dms/image/v2/C4E22AQE-PVFtSKhZ9Q/feedshare-shrink_800/feedshare-shrink_800/0/1672759695529?e=2147483647&v=beta&t=7wbwuytXbyg0kUZt8rFaC6wJymEgPCbz5gKuhyO2JuA";

export default function BeTheRippleLanding() {
  const [showForm, setShowForm] = useState(false);
  const [formData, setFormData] = useState({ name: "", email: "" });

  const handleChange = (e) => {
    const { name, value } = e.target;
    setFormData((prev) => ({ ...prev, [name]: value }));
  };

  const handleSubmit = (e) => {
    e.preventDefault();
    confetti({
      particleCount: 200,
      spread: 100,
      origin: { y: 0.6 },
    });
    alert(`Thank you, ${formData.name}! We will contact you at ${formData.email}.`);
    setFormData({ name: "", email: "" });
    setShowForm(false);
  };

  return (
    <div
      className="min-h-screen text-left px-4 py-12 font-sans bg-cover bg-no-repeat relative text-white"
      style={{ backgroundImage: `url(${backgroundImageUrl})`, backgroundPosition: "center 30%" }}
    >
      {/* White header at the top */}
      <div className="w-full h-16 bg-white absolute top-0 left-0 z-20"></div>

      <div className="absolute top-20 right-7 z-10">
        <ul className="flex flex-wrap justify-end gap-6 text-white text-sm md:text-base">
          <li className="cursor-pointer border-b-2 border-yellow-400 pb-1">About</li>
          <li className="cursor-pointer border-b-2 border-yellow-400 pb-1">How</li>
          <li className="cursor-pointer border-b-2 border-yellow-400 pb-1">People</li>
          <li className="cursor-pointer border-b-2 border-yellow-400 pb-1">Places</li>
          <li className="cursor-pointer border-b-2 border-yellow-400 pb-1">Give</li>
        </ul>
      </div>
      <div className="max-w-3xl relative z-10 text-left">
        <img
          src="https://paytaxeslater.com/wp-content/uploads/2018/05/CharityWater.jpg"
          alt="Charity Water Logo"
          className="w-24 md:w-32 mb-6"
        />
        <h1 className="text-4xl md:text-5xl font-bold leading-tight mb-6">
          Be the Ripple <br className="hidden md:block" /> That Creates{" "}
          <span className="text-yellow-400">Waves</span>
        </h1>
        <p className="text-lg md:text-xl mb-10 leading-relaxed md:leading-loose max-w-[32rem]">
          <strong>Join the global movement</strong> bringing clean water to communities around the world. <strong>Every dollar you give</strong> goes straight to the field, proving that <strong>purpose, not money</strong>, is what drives <span className="text-yellow-400 font-bold">real change</span>.
        </p>
        <button
          onClick={() => setShowForm(true)}
          className="bg-yellow-400 hover:bg-yellow-500 text-black font-semibold py-3 px-8 rounded-full text-lg transition duration-300"
        >
          Start Your Ripple Today 💧!
        </button>

        {showForm && (
          <div className="mt-8 bg-white bg-opacity-90 p-6 rounded-lg shadow-md text-black relative">
            <button
              onClick={() => setShowForm(false)}
              className="absolute top-2 right-2 text-gray-600 hover:text-gray-900 font-bold"
              aria-label="Close form"
            >
              &times;
            </button>
            <h2 className="text-xl font-semibold mb-4">Join the Movement 🚀</h2>
            <form className="space-y-4" onSubmit={handleSubmit}>
              <div>
                <label className="block text-sm font-medium mb-1" htmlFor="name">
                  Name
                </label>
                <input
                  id="name"
                  name="name"
                  type="text"
                  value={formData.name}
                  onChange={handleChange}
                  className="w-full px-4 py-2 bg-yellow-200 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-yellow-400 text-black"
                  placeholder="Your Name"
                  required
                />
              </div>
              <div>
                <label className="block text-sm font-medium mb-1" htmlFor="email">
                  Email
                </label>
                <input
                  id="email"
                  name="email"
                  type="email"
                  value={formData.email}
                  onChange={handleChange}
                  className="w-full px-4 py-2 bg-yellow-200 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-yellow-400 text-black"
                  placeholder="you@example.com"
                  required
                />
              </div>
              <button
                type="submit"
                className="bg-yellow-400 hover:bg-yellow-500 text-black font-semibold py-2 px-6 rounded-full transition duration-300"
              >
                Submit
              </button>
            </form>
          </div>
        )}
      </div>
    </div>
  );
}
