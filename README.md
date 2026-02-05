# will you be my valentines? :3 
    <div className="min-h-screen bg-white flex flex-col items-center justify-center p-4">
      <div className="text-center max-w-md">
        <img
          src="https://horizons-cdn.hostinger.com/784f5e44-8807-43fa-94f1-8d1c6b63b441/b7d7ea536afb499af93aec1aa6b40545.gif"
          alt="Jake the Dog from Adventure Time"
          className="w-48 h-auto mx-auto mb-6"
        />

        <h1 className="text-5xl font-bold text-gray-800 mb-12">
          Will you be my valentine?
        </h1>

        {response === null && (
          <div className="flex gap-6 justify-center">
            <button
              onClick={handleYes}
              className="px-8 py-3 bg-gray-500 text-white font-semibold rounded-lg hover:bg-gray-600 transition-colors duration-200"
            >
              Yes
            </button>
            <button
              onClick={handleNo}
              className="px-8 py-3 bg-gray-400 text-white font-semibold rounded-lg hover:bg-gray-500 transition-colors duration-200"
            >
              No
            </button>
          </div>
        )}

        {response === 'yes' && (
          <div className="text-center">
            <p className="text-3xl font-bold text-green-600 mb-6">
              Yay! 💕
            </p>
            <button
              onClick={handleReset}
              className="px-6 py-2 bg-gray-300 text-gray-800 font-semibold rounded-lg hover:bg-gray-400 transition-colors duration-200"
            >
              Ask Again
            </button>
          </div>
        )}

        {response === 'no' && (
          <div className="text-center">
            <p className="text-3xl font-bold text-orange-600 mb-6">
              Are you sure? 💔
            </p>
            <button
              onClick={handleReset}
              className="px-6 py-2 bg-gray-300 text-gray-800 font-semibold rounded-lg hover:bg-gray-400 transition-colors duration-200"
            >
              Try Again
            </button>
          </div>
        )}
      </div>
    </div>
  );
};

export default ValentinesPage;
