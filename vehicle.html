// ===== TopWheels Int, Auto Sales LLC - main.js =====

const INVENTORY = [
  { id:"tw-1001", year:2021, make:"Toyota", model:"Camry", trim:"SE", price:24990, miles:38420, fuel:"Gas", drivetrain:"FWD", tag:"Certified" },
  { id:"tw-1002", year:2020, make:"Honda", model:"Civic", trim:"Sport", price:21990, miles:41210, fuel:"Gas", drivetrain:"FWD", tag:"Sport" },
  { id:"tw-1003", year:2022, make:"Ford", model:"F-150", trim:"XLT", price:42990, miles:26880, fuel:"Gas", drivetrain:"4WD", tag:"Truck" },
  { id:"tw-1004", year:2021, make:"BMW", model:"330i", trim:"", price:35990, miles:29500, fuel:"Gas", drivetrain:"RWD", tag:"Premium" },
  { id:"tw-1005", year:2019, make:"Jeep", model:"Grand Cherokee", trim:"", price:27990, miles:55800, fuel:"Gas", drivetrain:"4WD", tag:"SUV" },
  { id:"tw-1006", year:2023, make:"Tesla", model:"Model 3", trim:"", price:36990, miles:14250, fuel:"Electric", drivetrain:"RWD", tag:"EV" },
];

function money(n){
  return new Intl.NumberFormat("en-US",{style:"currency",currency:"USD",maximumFractionDigits:0}).format(n);
}
function number(n){
  return new Intl.NumberFormat("en-US").format(n);
}

function setYear(){
  const el = document.getElementById("year");
  if(el) el.textContent = new Date().getFullYear();
}

function renderInventoryCards(list){
  const grid = document.getElementById("inventoryGrid");
  if(!grid) return;

  grid.innerHTML = list.map(v => {
    const name = `${v.year} ${v.make} ${v.model}${v.trim ? " " + v.trim : ""}`;
    return `
      <a class="inv-card" href="vehicle.html?id=${encodeURIComponent(v.id)}">
        <div class="media">
          <span class="tag">${v.tag}</span>
        </div>
        <div class="body">
          <p class="title">${name}</p>
          <div class="meta">
            <span>${number(v.miles)} mi</span>
            <span>•</span>
            <span>${v.drivetrain}</span>
            <span>•</span>
            <span>${v.fuel}</span>
          </div>
          <div class="price">
            <span class="money">${money(v.price)}</span>
            <span class="small">View →</span>
          </div>
        </div>
      </a>
    `;
  }).join("");
}

function setupInventoryPage(){
  const grid = document.getElementById("inventoryGrid");
  if(!grid) return; // not on inventory page

  const searchEl = document.getElementById("search");
  const makeEl = document.getElementById("make");
  const fuelEl = document.getElementById("fuel");
  const priceEl = document.getElementById("price");
  const sortEl = document.getElementById("sort");
  const countEl = document.getElementById("resultCount");
  const clearBtn = document.getElementById("clearFilters");

  // Fill makes
  const makes = [...new Set(INVENTORY.map(v => v.make))].sort();
  makes.forEach(m => {
    const opt = document.createElement("option");
    opt.value = m;
    opt.textContent = m;
    makeEl.appendChild(opt);
  });

  function apply(){
    let list = [...INVENTORY];

    const q = (searchEl.value || "").trim().toLowerCase();
    const make = makeEl.value;
    const fuel = fuelEl.value;
    const price = priceEl.value;
    const sort = sortEl.value;

    if(q){
      list = list.filter(v => {
        const text = `${v.year} ${v.make} ${v.model} ${v.trim} ${v.tag} ${v.fuel} ${v.drivetrain}`.toLowerCase();
        return text.includes(q);
      });
    }
    if(make !== "Any") list = list.filter(v => v.make === make);
    if(fuel !== "Any") list = list.filter(v => v.fuel === fuel);

    if(price !== "Any"){
      if(price === "40000-max"){
        list = list.filter(v => v.price >= 40000);
      } else {
        const [min,max] = price.split("-").map(Number);
        list = list.filter(v => v.price >= min && v.price <= max);
      }
    }

    if(sort === "year-desc") list.sort((a,b)=> b.year - a.year);
    if(sort === "price-asc") list.sort((a,b)=> a.price - b.price);
    if(sort === "price-desc") list.sort((a,b)=> b.price - a.price);
    if(sort === "miles-asc") list.sort((a,b)=> a.miles - b.miles);

    renderInventoryCards(list);
    if(countEl) countEl.textContent = `${list.length} vehicle${list.length===1 ? "" : "s"}`;
  }

  // Events
  [searchEl, makeEl, fuelEl, priceEl, sortEl].forEach(el => {
    el.addEventListener("input", apply);
    el.addEventListener("change", apply);
  });

  if(clearBtn){
    clearBtn.addEventListener("click", () => {
      searchEl.value = "";
      makeEl.value = "Any";
      fuelEl.value = "Any";
      priceEl.value = "Any";
      sortEl.value = "year-desc";
      apply();
    });
  }

  apply();
}

document.addEventListener("DOMContentLoaded", () => {
  setYear();
  setupInventoryPage();
});
