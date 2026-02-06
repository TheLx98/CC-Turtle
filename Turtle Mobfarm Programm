-- melee.lua
-- Turtle schlägt permanent nach vorne.
-- Wenn Items ins Inventar kommen: alles nach unten ausgeben.

local function dropAllDown()
  for slot = 1, 16 do
    turtle.select(slot)
    if turtle.getItemCount(slot) > 0 then
      turtle.dropDown()
    end
  end
  turtle.select(1)
end

while true do
  -- "Mob steht vor ihr" kann die Turtle ohne Sensor nicht erkennen.
  -- Daher: Angriff als minimaler Test. Mehr tut sie nicht.
  turtle.attack()

  -- Falls Drops eingesammelt wurden, nach unten ausgeben
  dropAllDown()

  -- kurzer Sleep, damit sie nicht völlig sinnlos die TPS grillt
  os.sleep(0.1)
end
