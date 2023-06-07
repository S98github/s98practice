HomeController--
using System;
using System.Collections.Generic;
using System.Diagnostics;
using System.Linq;
using System.Threading.Tasks;
using Microsoft.AspNetCore.Mvc;
using Microsoft.Extensions.Logging;
using Exam.Models;

namespace Exam.Controllers;

    public class HomeController : Controller
    {
        public async Task<IActionResult> Index()
        {
        var model = new StockQuote { Symbol = "Welcome Suman!!", Price = 4000 };
            return View(model);
        }
    }

StockQuote--
using System;
namespace Exam.Models;
    public class StockQuote
{
    public string Symbol { get; set; }
    public int Price { get; set; }
}

Index--
@{
    ViewData["Title"] = "Home Page";
}

<div>
    Symbol:@Model.Symbol </br>
    Symbol:@Model.Price </br>
</div>


first--
using System;
using System.Collections.Generic;
using System.Diagnostics;
using System.Linq;
using System.Threading.Tasks;
using Microsoft.AspNetCore.Mvc;
using Microsoft.Extensions.Logging;
using Exam.Models;

namespace Exam.Controllers;

    public class HomeController : Controller
    {
        public string Index()
        {
            return "Welcome Suman";
        }
    }



