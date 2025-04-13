import React from "react"; import { Card, CardContent } from "@/components/ui/card"; import { Button } from "@/components/ui/button"; import { Input } from "@/components/ui/input"; import { Tabs, TabsContent, TabsList, TabsTrigger } from "@/components/ui/tabs";

export default function HomePage() { return ( <main className="p-4 max-w-3xl mx-auto bg-gradient-to-br from-blue-100 to-purple-200 min-h-screen rounded-xl shadow-xl"> <h1 className="text-3xl font-bold mb-6 text-center text-purple-800">BDIN P2P Marketplace</h1>

<Tabs defaultValue="buy" className="w-full">
    <TabsList className="grid grid-cols-2 w-full mb-6 bg-white rounded-xl overflow-hidden shadow-md">
      <TabsTrigger value="buy" className="p-3 text-purple-700 font-semibold">Buy Coin</TabsTrigger>
      <TabsTrigger value="sell" className="p-3 text-purple-700 font-semibold">Sell Coin</TabsTrigger>
    </TabsList>

    <TabsContent value="buy">
      <Card className="bg-white shadow-lg">
        <CardContent className="space-y-4 p-6">
          <h2 className="text-xl font-semibold text-purple-700">Create Buy Offer</h2>
          <Input placeholder="Amount in your currency (e.g., INR, BDT, PKR)" className="rounded-xl" />
          <Input placeholder="Preferred Payment Method (e.g. bKash, Paytm)" className="rounded-xl" />
          <Input placeholder="Your Country" className="rounded-xl" />
          <Button className="bg-purple-600 hover:bg-purple-700 text-white w-full rounded-xl">Post Buy Offer</Button>
        </CardContent>
      </Card>
    </TabsContent>

    <TabsContent value="sell">
      <Card className="bg-white shadow-lg">
        <CardContent className="space-y-4 p-6">
          <h2 className="text-xl font-semibold text-purple-700">Create Sell Offer</h2>
          <Input placeholder="Amount in BDIN coin" className="rounded-xl" />
          <Input placeholder="Payment Method You Accept" className="rounded-xl" />
          <Input placeholder="Your Country" className="rounded-xl" />
          <Button className="bg-purple-600 hover:bg-purple-700 text-white w-full rounded-xl">Post Sell Offer</Button>
        </CardContent>
      </Card>
    </TabsContent>
  </Tabs>

  <section className="mt-10">
    <h2 className="text-2xl font-bold mb-4 text-purple-800 text-center">Available Offers Near You</h2>
    <div className="grid grid-cols-1 md:grid-cols-2 gap-4">
      <Card className="bg-white shadow-md">
        <CardContent className="p-4 space-y-2">
          <p><strong>User:</strong> @Rafi</p>
          <p><strong>Wants to Buy:</strong> 500 Taka worth of BDIN</p>
          <p><strong>Payment Method:</strong> bKash</p>
          <Button className="bg-green-500 hover:bg-green-600 text-white w-full rounded-xl">Trade Now</Button>
        </CardContent>
      </Card>

      <Card className="bg-white shadow-md">
        <CardContent className="p-4 space-y-2">
          <p><strong>User:</strong> @Anjali</p>
          <p><strong>Wants to Sell:</strong> 50 BDIN</p>
          <p><strong>Accepting:</strong> Paytm</p>
          <Button className="bg-green-500 hover:bg-green-600 text-white w-full rounded-xl">Trade Now</Button>
        </CardContent>
      </Card>
    </div>
  </section>

  <footer className="text-center mt-10 text-sm text-gray-600">
    Powered by BDIN | Safe P2P Transfers across BD, IN, PK
  </footer>
</main>

); }

