{
  "workflow": {
    "name": "Zalora Order Process",
    "steps": [
      {
        "name": "Open App/Website",
        "type": "start"
      },
      {
        "name": "Browse Products",
        "type": "process"
      },
      {
        "name": "Select Items & Add to Cart",
        "type": "process"
      },
      {
        "name": "Proceed to Checkout",
        "type": "process"
      },
      {
        "name": "Payment Processing",
        "type": "decision",
        "branches": [
          {
            "condition": "Payment Failed",
            "next_step": "Proceed to Checkout"
          },
          {
            "condition": "Payment Successful",
            "next_step": "Order Confirmation"
          }
        ]
      },
      {
        "name": "Order Confirmation",
        "type": "process"
      },
      {
        "name": "Warehouse Processing",
        "type": "process"
      },
      {
        "name": "Handover to Logistics",
        "type": "process"
      },
      {
        "name": "Shipping & Tracking",
        "type": "process"
      },
      {
        "name": "Delivery & Order Received",
        "type": "process"
      },
      {
        "name": "Post-Purchase Services",
        "type": "decision",
        "branches": [
          {
            "condition": "Leave a Review",
            "next_step": "End Process"
          },
          {
            "condition": "Request Return/Exchange",
            "next_step": "Return/Exchange Process"
          },
          {
            "condition": "Contact Customer Support",
            "next_step": "Customer Support Assistance"
          }
        ]
      },
      {
        "name": "Return/Exchange Process",
        "type": "process",
        "next_step": "End Process"
      },
      {
        "name": "Customer Support Assistance",
        "type": "process",
        "next_step": "End Process"
      },
      {
        "name": "End Process",
        "type": "end"
      }
    ]
  }
}


