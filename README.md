// Book Your Appointment - React Frontend (Starter Template)

import React from 'react'; import { BrowserRouter as Router, Route, Routes, Link } from 'react-router-dom'; import { Card, CardContent } from "@/components/ui/card"; import { Button } from "@/components/ui/button";

function Home() { return ( <div className="p-6 text-center"> <h1 className="text-4xl font-bold mb-4">Book Your Appointment</h1> <p className="text-lg mb-6">Easily schedule appointments with hospital specialists and access healthcare facilities online.</p> <Link to="/appointments"> <Button className="text-lg px-6 py-2">Book Now</Button> </Link> </div> ); }

function Appointments() { return ( <div className="p-6"> <h2 className="text-2xl font-semibold mb-4">Available Doctors</h2> <div className="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-4"> {["Dr. Smith - Cardiology", "Dr. Ayesha - Pediatrics", "Dr. Khan - Neurology"].map((doc, index) => ( <Card key={index} className="hover:shadow-lg transition"> <CardContent className="p-4"> <h3 className="text-lg font-medium">{doc}</h3> <p className="text-sm mt-2">Click below to book an appointment.</p> <Button className="mt-3">Book Appointment</Button> </CardContent> </Card> ))} </div> </div> ); }

function Contact() { return ( <div className="p-6"> <h2 className="text-2xl font-semibold mb-4">Contact Us</h2> <p>Email: support@hospital.com</p> <p>Phone: +123-456-7890</p> </div> ); }

