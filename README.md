req.user = await User.findOne({ _id }).select("_id");

This line search for the id of the logged in user and return that id to match with the ids of the tours and the todo tasks.